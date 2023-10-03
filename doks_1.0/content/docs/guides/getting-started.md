---
title: "Getting started"
description: "Getting started guide for BulkInsert, BulkUpdate and BulkDelete"
summary: "Getting Started with EF Box: Simplifying Bulk Insert, Update and Delete"
lead: ""
draft: false
images: []
menu:
  docs:
    parent: ""
    identifier: "getting-started"
weight: 100
toc: true
---

In this article, we'll dive into how you can utilize `BulkInsert`, `BulkUpdate`, and `BulkDelete` methods in EF Box to manage your data efficiently. The following code snippets demonstrates the creation of demo data, bulk insertion, updating, and deletion of records in your database. 

This is a straightforward way to handle large datasets with minimal code, showcasing the simplicity and effectiveness of EF Box in managing bulk operations.

## Preparing the Data Model

Before diving into bulk operations, it's crucial to understand the data model for our example. 

We define a  `Blog` class which represents a schema of blog entries, including properties like `BlogId`, `Url`, `Rating`, `DisplayUrl`, `CreationDate`, and `UpdateDate`. 

```C#
public class Blog
{
    public int BlogId { get; set; }
    public string Url { get; set; }
    public int? Rating { get; set; }
    public string DisplayUrl { get; set; }
    [Column("Created")]
    public DateTime? CreationDate { get; set; }
    [Column("Updated")]
    public DateTime? UpdateDate { get; set; }    
    //Properties below only needed for BulkMerge
    [NotMapped]
    public DateTime ChangeDate { get; set; }
    [NotMapped]
    public ChangeAction? ChangeAction { get; set; }
}
```

The `BloggingContext` class sets up the database context with a connection to a SQL Server database. The `OnModelCreating` method further configures the model, setting default values and computed columns. This setup enables Entity Framework to create the database table through migrations, laying the groundwork for the following bulk operation examples.

```C#
public class BloggingContext : DbContext
{
    public DbSet<Blog> Blogs { get; set; }

    public string DbPath { get; }

    public BloggingContext() {
    }

    protected override void OnConfiguring(DbContextOptionsBuilder options) {
        options.UseSqlServer($"Data Source=localhost;User Id=sa;Password=YourStrong@Passw0rd;Initial Catalog=efdemo;TrustServerCertificate=true");
    }

    protected override void OnModelCreating(ModelBuilder modelBuilder) {
        modelBuilder.Entity<Blog>()
            .Property(b => b.Rating)
            .HasDefaultValue(3);
        modelBuilder.Entity<Blog>()
            .Property(p => p.DisplayUrl)
             .HasComputedColumnSql("'https:'+[Url]");
        modelBuilder.Entity<Blog>()
        .Property(b => b.CreationDate)
        .HasDefaultValueSql("GETDATE()");

    }
}
```

### Creating the database table

As you're already acquainted with Entity Framework (EF), you'll recall that you can effortlessly scaffold a database using the `Add-Migration` command to generate migration scripts, and the `Update-Database` command to apply these migrations to your database. This mechanism ensures your database schema aligns seamlessly with your defined models, allowing for a smooth developmental workflow.
So we started to create our database table using both command, utilizing a code-first approach. {{< link-ext text="See the official docs for migrations in EF." url="https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli" >}}

## Bulk Insert

In the first part of the code, demo data is created using a simple loop, which generates a list of new blogs with unique URLs and ratings. The `BulkInsert` method is then used to add these entries to the database efficiently.

```C#
//Creating demo data
var data = new List<Blog>();
for (int i = 1; i <= 5000; i++) {
    var newBlog = new Blog {
        Url = $"blogs.msdn.com/{i}",
        Rating = i % 10
    };
    data.Add(newBlog);
}

//Bulk insert
db.BulkInsert(data);
```

## Bulk Update

For the update operation, the ratings and URLs of the existing data are modified. The `BulkUpdate` method swiftly reflects these changes in the database, showcasing its effectiveness in handling bulk updates.

```C#
for (int i=0;i< 4000;i++) {
    data[i].Rating = data[i].Rating * 10;
    data[i].Url = "https://" + data[i].Url;
    data[i].UpdateDate = DateTime.Now.ToUniversalTime();
}

//Bulk update - will ignore already inserted rows   
db.BulkUpdate(data);
```

## Bulk Delete 

Lastly, to demonstrate deletion, the `BulkDelete` method is employed to remove specified records from the database. This operation exemplifies how you can manage data deletions en masse, maintaining a clean and optimized database.

```C#
 var dataToDelete = data.Take(1000);
 db.BulkDelete();
 ```

 ## Bulk Merge

 Now let's have a look at the versatility of BulkMerge. The code snippet begins by loading existing data, then performs deletions, updates, and inserts on this data. It wraps up by syncing these changes with the database using BulkMerge with MergeMode set to Full. This single operation neatly encapsulates a series of data manipulations, showcasing BulkMerge as a potent tool for keeping your data in sync. 

 ```C#
//Load existing data 
var data = db.Blogs.ToList();

//Delete first X records from start
data.RemoveRange(0, 1000);

//Update first X records
for (int i = 0; i < 1000; i++) {
    data[i].Url = null;
    data[i].Rating = -1;
    data[i].UpdateDate = DateTime.Now.ToUniversalTime();
}

//Append new records at end
for (int i = 0; i <= 1000; i++) {
    var newBlog = new Blog {
        Url = $"blogs.msdn.com/{i}",                
        CreationDate = DateTime.Now.ToUniversalTime(),                
    };
    data.Add(newBlog);
}

//Sync with table
db.BulkMerge(data, options => options.MergeMode = MergeMode.Full);
```

The `MergeMode.Full` setting ensures a complete sync, including deletion of data not present in our list. Other modes like `Delta`, `InsertsAndUpdates`, `InsertsOnly`, and `UpdatesOnly` offer different sync scopes. Unlike other bulk operations, `BulkMerge` reads existing rows first from the database, and then determines the corresponding batch operations. It logs the merge result in `ChangeAction` (e.g.,Insert, Update, Delete or Exists) and timestamps in the `ChangeDate` property. You will need to add both properties to your class - ensure that they are marked with `[NotMapped]` to avoid database mapping.


## Full Example on GitHub

The entire example, including the code snippets discussed, {{< link-ext text="is available on GitHub" url="https://github.com/etlbox/etlbox.demo/tree/main/EF_GettingStarted" >}}. Feel free to explore it further for a deeper understanding of EF Box and its capabilities.