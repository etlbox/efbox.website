---
title: "DbContextExtensions"
description: "Details for Class DbContextExtensions (EFBox.SqlServer)"
draft: false
images: []
menu:
  api:
    parent: "efbox.sqlserver"
weight: 10006
toc: false
---

{{< rawhtml >}}

            <article class="content wrap" id="_content" data-uid="EFBox.SqlServer.DbContextExtensions">
  <h1 id="EFBox_SqlServer_DbContextExtensions" data-uid="EFBox.SqlServer.DbContextExtensions" class="text-break">Class DbContextExtensions
</h1>
  <div class="markdown level0 summary"><p>Extending your DbContext with the missing bulk operations for SqlServer</p>
</div>
  <div class="markdown level0 conceptual"></div>
  <div class="inheritance">
    <h5>Inheritance</h5>
    <div class="level0"><span class="xref">System.Object</span></div>
    <div class="level1"><span class="xref">DbContextExtensions</span></div>
  </div>
<h6><strong>Namespace</strong>: EFBox.SqlServer</h6>
  <h6><strong>Assembly</strong>: EFBox.SqlServer.dll</h6>
  <h5 id="EFBox_SqlServer_DbContextExtensions_syntax">Syntax</h5>
{{< /rawhtml >}}

```C#
    public static class DbContextExtensions
```

{{< rawhtml >}}
  <h3 id="methods">Methods
</h3>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkDelete_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkDelete*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkDelete__1_DbContext_IEnumerable___0__Action_EFBox_BulkOptions___0___" data-uid="EFBox.SqlServer.DbContextExtensions.BulkDelete``1(DbContext,IEnumerable{``0},Action{EFBox.BulkOptions{``0}})">BulkDelete&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;, Action&lt;BulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you delete a large number of records in your database by utilizing bulk delete sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkDelete<T>(this DbContext dbContext, IEnumerable<T> entities, Action<BulkOptions<T>> options)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records for deletion</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">Action&lt;&gt;</span>&lt;<a class="xref" href="/docs/api/efbox/bulkoptions-1">BulkOptions</a>&lt;T&gt;&gt;</td>
        <td><span class="parametername">options</span></td>
        <td><p>Configurable options for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkDelete_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkDelete*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkDelete__1_DbContext_IEnumerable___0__" data-uid="EFBox.SqlServer.DbContextExtensions.BulkDelete``1(DbContext,IEnumerable{``0})">BulkDelete&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you delete a large number of records in your database by utilizing bulk delete sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkDelete<T>(this DbContext dbContext, IEnumerable<T> entities)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records for deletion</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkInsert_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkInsert*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkInsert__1_DbContext_IEnumerable___0__Action_EFBox_BulkOptions___0___" data-uid="EFBox.SqlServer.DbContextExtensions.BulkInsert``1(DbContext,IEnumerable{``0},Action{EFBox.BulkOptions{``0}})">BulkInsert&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;, Action&lt;BulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you insert a large number of records in your database by utilizing bulk insert sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkInsert<T>(this DbContext dbContext, IEnumerable<T> entities, Action<BulkOptions<T>> options)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records for insertion</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">Action&lt;&gt;</span>&lt;<a class="xref" href="/docs/api/efbox/bulkoptions-1">BulkOptions</a>&lt;T&gt;&gt;</td>
        <td><span class="parametername">options</span></td>
        <td><p>Configurable options for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkInsert_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkInsert*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkInsert__1_DbContext_IEnumerable___0__" data-uid="EFBox.SqlServer.DbContextExtensions.BulkInsert``1(DbContext,IEnumerable{``0})">BulkInsert&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you insert a large number of records in your database by utilizing bulk insert sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkInsert<T>(this DbContext dbContext, IEnumerable<T> entities)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records for insertion</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkMerge_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkMerge*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkMerge__1_DbContext_IEnumerable___0__Action_EFBox_MergeBulkOptions___0___" data-uid="EFBox.SqlServer.DbContextExtensions.BulkMerge``1(DbContext,IEnumerable{``0},Action{EFBox.MergeBulkOptions{``0}})">BulkMerge&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;, Action&lt;MergeBulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you sync a large number of records in your database by utilizing bulk sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkMerge<T>(this DbContext dbContext, IEnumerable<T> entities, Action<MergeBulkOptions<T>> options)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records to merge</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">Action&lt;&gt;</span>&lt;<a class="xref" href="/docs/api/efbox/mergebulkoptions-1">MergeBulkOptions</a>&lt;T&gt;&gt;</td>
        <td><span class="parametername">options</span></td>
        <td><p>Configurable options for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkMerge_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkMerge*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkMerge__1_DbContext_IEnumerable___0__" data-uid="EFBox.SqlServer.DbContextExtensions.BulkMerge``1(DbContext,IEnumerable{``0})">BulkMerge&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you sync a large number of records in your database by utilizing bulk sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkMerge<T>(this DbContext dbContext, IEnumerable<T> entities)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records to merge</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkUpdate_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkUpdate*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkUpdate__1_DbContext_IEnumerable___0__Action_EFBox_BulkOptions___0___" data-uid="EFBox.SqlServer.DbContextExtensions.BulkUpdate``1(DbContext,IEnumerable{``0},Action{EFBox.BulkOptions{``0}})">BulkUpdate&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;, Action&lt;BulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you update a large number of records in your database by utilizing bulk udpate sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkUpdate<T>(this DbContext dbContext, IEnumerable<T> entities, Action<BulkOptions<T>> options)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records to update</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">Action&lt;&gt;</span>&lt;<a class="xref" href="/docs/api/efbox/bulkoptions-1">BulkOptions</a>&lt;T&gt;&gt;</td>
        <td><span class="parametername">options</span></td>
        <td><p>Configurable options for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_SqlServer_DbContextExtensions_BulkUpdate_" data-uid="EFBox.SqlServer.DbContextExtensions.BulkUpdate*"></a>
  <h4 id="EFBox_SqlServer_DbContextExtensions_BulkUpdate__1_DbContext_IEnumerable___0__" data-uid="EFBox.SqlServer.DbContextExtensions.BulkUpdate``1(DbContext,IEnumerable{``0})">BulkUpdate&lt;T&gt;(DbContext, IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you update a large number of records in your database by utilizing bulk udpate sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public static void BulkUpdate<T>(this DbContext dbContext, IEnumerable<T> entities)
```

{{< rawhtml >}}
  <h5 class="parameters">Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td><span class="parametername">dbContext</span></td>
        <td><p>Extending your current DbContext</p>
</td>
      </tr>
      <tr>
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">entities</span></td>
        <td><p>Records to update</p>
</td>
      </tr>
    </tbody>
  </table>
  <h5 class="typeParameters">Type Parameters</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Name</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="parametername">T</span></td>
        <td><p>EF Data type that maps with your table</p>
</td>
      </tr>
    </tbody>
  </table>

{{< /rawhtml >}}
