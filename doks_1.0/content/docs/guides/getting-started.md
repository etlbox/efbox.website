---
title: "Getting started"
description: ""
summary: ""
draft: false
images: []
menu:
  docs:
    parent: ""
    identifier: "example-6a1a6be4373e933280d78ea53de6158e"
weight: 810
toc: true
---

```c#
// Initiating a new database context
using (var db = new Context()) {
   // Crafting a collection of demo data
   var data = CreateDemoDataCollection();
   // Employing BulkInsert to swiftly add the data to the database
   db.BulkInsert(data);
}
```
