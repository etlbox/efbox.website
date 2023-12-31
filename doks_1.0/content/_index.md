---
title : "Entity Framework Box"
description: "Entity Framework Box Start page"
summary: "Start page - Bridging ETLBox and Entity Framework with seamless DbContext extensions for efficient bulk operations!"
lead: "Bridging ETLBox and Entity Framework with seamless DbContext extensions for efficient bulk operations!"
draft: false
images: []
---

##### Effortless Data Insertion with BulkInsert

```C#
// Initiating a new database context
using (var db = new Context()) {
   // Crafting a collection of demo data
   var data = CreateDemoDataCollection();
   // Employing BulkInsert to swiftly add the data to the database
   db.BulkInsert(data);
}
```

In this snippet, we create a database context and demo data, then use `BulkInsert()` to quickly add all data to the database. Simple and fast!

##### Swift Data Modification with BulkUpdate

```csharp
// Initiating a new database context
using (var db = new Context()) {
   // Crafting a collection of demo data for update
   var data = UpdateDemoDataCollection();
   // Employing BulkUpdate to swiftly modify the data in the database
   db.BulkUpdate(data);
}
```

Here,we create a database context and demo data, then use `BulkUpdate()` to quickly update the dataset. Fast and simple!

##### Streamlined Data Removal with BulkDelete()

```C#
// Initiating a new database context
using (var db = new Context()) {
   // Preparing a collection of demo data for deletion
   var dataToDelete = DeleteDemoDataCollection();
   // Using BulkDelete to swiftly remove the data from the database
   db.BulkDelete(dataToDelete);
}
```

Here we create a database context and demo data for deletion, then use `BulkDelete()` to efficiently remove the specified records from the database. Quick and clean!

##### One-Step Data Sync with BulkMerge

```C#
// Initiating a new database context
using (var db = new Context()) {
   // Crafting collections of demo data for insert and update
   var dataToInsert = InsertDemoDataCollection();
   var dataToUpdate = UpdateDemoDataCollection();

   // Merging both data collections into one
   var mergedData = dataToInsert.Union(dataToUpdate);

   // Employing BulkMerge to handle insert, update, and delete operations seamlessly
   db.BulkMerge(mergedData, options => options.MergeMode = MergeMode.Full);
}
```

Now we employ `BulkMerge()` with `MergeMode` set to `Full`. This way, EFBox smartly handles not only the insertion and updating of data but also identifies and deletes any obsolete records, all in one swift operation. Your data sync tasks just got a whole lot easier and faster!

## Kickstart EFBox

Ready to turbocharge your database operations with EFBox? Select your flavor:

- SQL Server aficionado? Grab {{<link-ext text="<code>EFBox.SqlServer</code>" url="https://www.nuget.org/packages/EFBox.SqlServer">}}
- MySQL enthusiast? Snag {{<link-ext text="<code>EFBox.MySql</code>" url="https://www.nuget.org/packages/EFBox.MySql">}}
- PostgreSQL fan? Pick {{<link-ext text="<code>EFBox.Postgres</code>" url="https://www.nuget.org/packages/EFBox.Postgres">}}

Install via NuGet Package Manager, dash through the Package Manager Console, or command the dotnet CLI. Match your database, install, and you're on the fast track!