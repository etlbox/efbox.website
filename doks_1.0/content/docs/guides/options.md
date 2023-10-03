---
title: "Option Tuning"
description: "Configuring EFBox Options for Optimized Bulk Operations"
summary: "Deep dive into configuring bulk operations in EFBox, explaining shared and specific options, including examples."
lead: ""
draft: false
images: []
menu:
  docs:
    parent: ""
    identifier: "options"
weight: 810
toc: true
---

When performing bulk operations, having a robust set of configurable options is essential. These shared bulk options allow you to define the batch size, handle errors, manage identity inserts, and track operation progress among others, ensuring a seamless data processing experience. While most options are common across all bulk operations, some are unique to specific tasks. For instance, there are exclusive settings for BulkMerge operations, allowing fine-tuned control over merging and caching behavior. On the flip side, BulkInsert, BulkUpdate, and BulkDelete also have distinct options enabling pre and post batch processing adjustments.

## Using options

In each bulk operation, you can configure various options by passing an `Action<BulkOptions>` (or `Action<MergeBulkOptions`) to the method. The example demonstrates setting multiple options within the `BulkInsert` operation. Each option is set within the lambda expression, allowing tailored behavior like specifying the `BatchSize` or action to track  progress.

```c#
db.BulkInsert(data, options => {
     options.BatchSize = 2;    
     options.OnProgress = _ => progress_count++;
});
```

## Shared options

The following options are relevant for all bulk operations.

### Batch Size

The `BatchSize` option determines the number of records processed in a single batch. Setting this to 10000, as shown, instructs `BulkInsert` to handle data in chunks of 10000 records per batch, optimizing performance when managing hefty datasets. By default, `BatchSize` is set to 1000.

```c#
db.BulkInsert(data, options => {
    options.BatchSize = 10000;
});
```


### Tracking progress

With the `OnProgress` option in EFBox, keep a tab on the progress of your bulk insert operation. This example demonstrates how you can increment a counter each time a batch is processed, providing a simple way to track how many batches have been handled during the operation. It's a handy feature for logging or user feedback during large bulk operations.

db.BulkInsert(data, options => {
   options.OnProgress = _ => count++;
});

### Data Transformation with ColumnConverters

The `ColumnConverters` option in EFBox allows you to apply transformations to data during bulk operations. In this example, a `ColumnConverter` is defined to prepend "https://" to the `Url` property of each record before it's inserted into the database. This is a powerful feature for applying quick data transformations without the need for manual data manipulation before executing the bulk operation.

```C#
db.BulkInsert(data, options => {                    
    options.ColumnConverters = new[] {
        new ColumnConverter() {
            ColumnName = "Url",
            ConversionFunc = u => "https://"+u.ToString()
        }
    };
});
```

### Skipping Back-Read of Generated Values

The `ReadGeneratedValues` option allows you to control whether to read back generated values like auto-incremented IDs from the database after a bulk operation. By default, this option is set to `true`. However, in scenarios where reading back generated values is not required, setting `ReadGeneratedValues` to `false` as shown in the example can enhance performance by reducing the back-and-forth communication with the database.

```C#
db.BulkInsert(data, options => options.ReadGeneratedValues = false);
```

### Enabling Identity Insert

The `AllowIdentityInsert` option allows you to override existing values in identity/auto-increment/serial columns during a bulk operation. By default, this option is set to `false`. When set to `true` as shown in the example, it enables identity insert, permitting the insertion of explicit values into the identity column of a table. This is useful when you need to keep identity values consistent between your data source and the database.

```C#
db.BulkInsert(data, options => options.AllowIdentityInsert = true);
```

### Redirecting Erroneous Batches

The `RedirectErroneousBatches` option, when set to `true`, allows the continuation of the bulk operation even when a batch encounters an error. Instead of halting the operation, the erroneous batches are redirected, preventing an exception from being thrown. The `BatchSize` is set to `2` in this example, defining the number of records to be processed in a single batch. This way, if an error occurs, the operation won’t stop, and you can later analyze what went wrong with the particular batches.

```C#
List<ETLBoxError> errors = new List<ETLBoxError>();
db.BulkInsert(data, options => {
    options.BatchSize = 2;
    options.RedirectErroneousBatches = true;
});
```

## Options for insert/update/delete

The following options are only relevant for the `BulkInsert`/`BulkUpdate`/`BulkDelete` operations.

### Before/After BatchWrite

Utilize the `BeforeBatchWrite` and `AfterBatchWrite` options in EFBox to interact with your data right before and after it's written in each batch during a bulk insert operation. In this example, `BeforeBatchWrite` is used to modify data if the batch size is greater than 2, while `AfterBatchWrite` helps in aggregating the count of processed records. Through these options you can access each batch of data before or after the bulk operation. 

```c#
db.BulkInsert(data, options => {
    options.AfterBatchWrite = b => {
        count += b.Length;
    };
    options.BeforeBatchWrite = b => {
      if (b.Length > 2) {
        b.ElementAt(0).Url = "test1";
        b.ElementAt(1).Url = "test2";
      }
      return b;      
    };
});
```

## Options for merge

The following options are only relevant for the `BulkMerge`. 

#### Changing merge mode

By default, `MergeMode.Full` is selected, enabling insert, update, and delete operations to synchronize data. Here are the available merge modes:

- `Delta`: Performs inserts and updates, with deletions only marked with a flag.
- `Full`: Executes inserts, updates, and deletions (deletions if a record is missing).
- `InsertsAndUpdates`: Allows inserts and updates only, ignoring deletion flags.
- `InsertsOnly`: Solely performs inserts, no updates or deletions.
- `UpdatesOnly`: Only allows updates, no inserts or deletions.

#### Setting Cache Modes

In this example, the `MergeMode` is set to `Delta` and `CacheMode` is set to `Partial` using the options parameter in the `BulkInsert` method. By default, the bulk merge will load all data from the destination into memory first before syncing data. If the target table is quite large and you wish to avoid this, consider setting the `CacheMode` to `Partial`. However, note that this will only work for merge modes other than `MergeMode.Full`, as in `Full` mode all data needs to be loaded into memory to detect the missing data (the deletes), balancing between performance and memory consumption.

```C#
db.BulkInsert(data, options => {
    options.MergeMode = MergeMode.Delta;
    options.CacheMode = CacheMode.Partial;
});
```

#### Customizing columns for Merge Operations

- `CompareColumns`: Define properties to check for equality during merge to decide if an update is needed.
- `UpdateColumns`: Specify properties to be updated when a row needs updating, by default all non-ID columns are updated.
- `DeleteColumns`: List property names along with a specific value indicating if a row is eligible for deletion during the merge operation. This option provides a way to mark rows for deletion based on certain criteria. Note: This option is only applicable when the MergeMode is set to Delta.

In merge operations, the property name is typically mapped to the column name as per Entity Framework conventions. However, you may need to specify which properties to use for comparing, updating, or deleting records. These options provide that flexibility.

```C#
 var compareColumns = new[] {
     new CompareColumn() {
         ComparePropertyName= nameof(Blog.Url),
     }
 };

 var updateColumns = new[] {
     new UpdateColumn() {
         UpdatePropertyName= nameof(Blog.Rating),
     }
 };

 var deleteColumns = new[] {
     new DeleteColumn() {
         DeletePropertyName = nameof(Blog.BlogId),
         DeleteOnMatchValue = 2
     }
 };

db.BulkMerge(data, options => {
    options.MergeMode = MergeMode.Delta;
    options.UpdateColumns = updateColumns;
    options.CompareColumns = compareColumns;
    options.DeleteColumns = deleteColumns;
});
```

In the provided example, the `CompareColumns` is set to compare the `Url` property, `UpdateColumns` is set to update the `Rating` property, and `DeleteColumns` is set to delete a row if the `BlogId` property matches the value 2. These configurations are utilized by the `BulkMerge` operation to determine how to synchronize the data with the database.