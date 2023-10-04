---
title: "BulkOperations"
description: "Details for Class BulkOperations (EFBox)"
draft: false
images: []
menu:
  api:
    parent: "efbox"
weight: 10000
toc: false
---

{{< rawhtml >}}

            <article class="content wrap" id="_content" data-uid="EFBox.BulkOperations">
  <h1 id="EFBox_BulkOperations" data-uid="EFBox.BulkOperations" class="text-break">Class BulkOperations
</h1>
  <div class="markdown level0 summary"><p>Base class that is used for creating ETLBox bulk operations.</p>
</div>
  <div class="markdown level0 conceptual"></div>
  <div class="inheritance">
    <h5>Inheritance</h5>
    <div class="level0"><span class="xref">System.Object</span></div>
    <div class="level1"><span class="xref">BulkOperations</span></div>
  </div>
<h6><strong>Namespace</strong>: EFBox</h6>
  <h6><strong>Assembly</strong>: EFBox.dll</h6>
  <h5 id="EFBox_BulkOperations_syntax">Syntax</h5>
{{< /rawhtml >}}

```C#
    public class BulkOperations
```

{{< rawhtml >}}
  <h3 id="constructors">Constructors
</h3>
  <a id="EFBox_BulkOperations__ctor_" data-uid="EFBox.BulkOperations.#ctor*"></a>
  <h4 id="EFBox_BulkOperations__ctor" data-uid="EFBox.BulkOperations.#ctor">BulkOperations()</h4>
  <div class="markdown level1 summary"></div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public BulkOperations()
```

{{< rawhtml >}}
  <a id="EFBox_BulkOperations__ctor_" data-uid="EFBox.BulkOperations.#ctor*"></a>
  <h4 id="EFBox_BulkOperations__ctor_DbContext_ETLBox_IConnectionManager_" data-uid="EFBox.BulkOperations.#ctor(DbContext,ETLBox.IConnectionManager)">BulkOperations(DbContext, IConnectionManager)</h4>
  <div class="markdown level1 summary"></div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public BulkOperations(DbContext context, IConnectionManager connectionManager)
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
        <td><span class="parametername">context</span></td>
        <td></td>
      </tr>
      <tr>
        <td><span class="xref">ETLBox.IConnectionManager</span></td>
        <td><span class="parametername">connectionManager</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations__ctor_" data-uid="EFBox.BulkOperations.#ctor*"></a>
  <h4 id="EFBox_BulkOperations__ctor_DbContext_" data-uid="EFBox.BulkOperations.#ctor(DbContext)">BulkOperations(DbContext)</h4>
  <div class="markdown level1 summary"></div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public BulkOperations(DbContext context)
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
        <td><span class="parametername">context</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <h3 id="properties">Properties
</h3>
  <a id="EFBox_BulkOperations_ConnectionManager_" data-uid="EFBox.BulkOperations.ConnectionManager*"></a>
  <h4 id="EFBox_BulkOperations_ConnectionManager" data-uid="EFBox.BulkOperations.ConnectionManager">ConnectionManager</h4>
  <div class="markdown level1 summary"><p>An ETLBox <span class="xref">ETLBox.IConnectionManager</span> used to wrap the current ADO.NET
connection manager.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public IConnectionManager ConnectionManager { get; set; }
```

{{< rawhtml >}}
  <h5 class="propertyValue">Property Value</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">ETLBox.IConnectionManager</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_DbConnectionManager_" data-uid="EFBox.BulkOperations.DbConnectionManager*"></a>
  <h4 id="EFBox_BulkOperations_DbConnectionManager" data-uid="EFBox.BulkOperations.DbConnectionManager">DbConnectionManager</h4>
  <div class="markdown level1 summary"></div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    protected virtual IConnectionManager DbConnectionManager { get; }
```

{{< rawhtml >}}
  <h5 class="propertyValue">Property Value</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">ETLBox.IConnectionManager</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_DbContext_" data-uid="EFBox.BulkOperations.DbContext*"></a>
  <h4 id="EFBox_BulkOperations_DbContext" data-uid="EFBox.BulkOperations.DbContext">DbContext</h4>
  <div class="markdown level1 summary"><p>Your current DbContext.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public DbContext DbContext { get; set; }
```

{{< rawhtml >}}
  <h5 class="propertyValue">Property Value</h5>
  <table class="table table-bordered table-striped table-condensed">
    <thead>
      <tr>
        <th>Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="xref">DbContext</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <h3 id="methods">Methods
</h3>
  <a id="EFBox_BulkOperations_BulkDelete_" data-uid="EFBox.BulkOperations.BulkDelete*"></a>
  <h4 id="EFBox_BulkOperations_BulkDelete__1_IEnumerable___0__Action_EFBox_BulkOptions___0___" data-uid="EFBox.BulkOperations.BulkDelete``1(IEnumerable{``0},Action{EFBox.BulkOptions{``0}})">BulkDelete&lt;T&gt;(IEnumerable&lt;T&gt;, Action&lt;BulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you delete a large number of records in your database by utilizing bulk delete sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkDelete<T>(IEnumerable<T> newRecords, Action<BulkOptions<T>> options)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for deletion</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkDelete_" data-uid="EFBox.BulkOperations.BulkDelete*"></a>
  <h4 id="EFBox_BulkOperations_BulkDelete__1_IEnumerable___0__" data-uid="EFBox.BulkOperations.BulkDelete``1(IEnumerable{``0})">BulkDelete&lt;T&gt;(IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you delete a large number of records in your database by utilizing bulk delete sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkDelete<T>(IEnumerable<T> newRecords)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for deletion</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkInsert_" data-uid="EFBox.BulkOperations.BulkInsert*"></a>
  <h4 id="EFBox_BulkOperations_BulkInsert__1_IEnumerable___0__Action_EFBox_BulkOptions___0___" data-uid="EFBox.BulkOperations.BulkInsert``1(IEnumerable{``0},Action{EFBox.BulkOptions{``0}})">BulkInsert&lt;T&gt;(IEnumerable&lt;T&gt;, Action&lt;BulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you insert a large number of records in your database by utilizing bulk insert sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkInsert<T>(IEnumerable<T> newRecords, Action<BulkOptions<T>> options)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for insertion</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkInsert_" data-uid="EFBox.BulkOperations.BulkInsert*"></a>
  <h4 id="EFBox_BulkOperations_BulkInsert__1_IEnumerable___0__" data-uid="EFBox.BulkOperations.BulkInsert``1(IEnumerable{``0})">BulkInsert&lt;T&gt;(IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you insert a large number of records in your database by utilizing bulk insert sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkInsert<T>(IEnumerable<T> newRecords)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for insertion</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkMerge_" data-uid="EFBox.BulkOperations.BulkMerge*"></a>
  <h4 id="EFBox_BulkOperations_BulkMerge__1_IEnumerable___0__Action_EFBox_MergeBulkOptions___0___" data-uid="EFBox.BulkOperations.BulkMerge``1(IEnumerable{``0},Action{EFBox.MergeBulkOptions{``0}})">BulkMerge&lt;T&gt;(IEnumerable&lt;T&gt;, Action&lt;MergeBulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you merge a large number of records in your database by utilizing bulk sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkMerge<T>(IEnumerable<T> newRecords, Action<MergeBulkOptions<T>> options)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for syncing</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkMerge_" data-uid="EFBox.BulkOperations.BulkMerge*"></a>
  <h4 id="EFBox_BulkOperations_BulkMerge__1_IEnumerable___0__" data-uid="EFBox.BulkOperations.BulkMerge``1(IEnumerable{``0})">BulkMerge&lt;T&gt;(IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you merge a large number of records in your database by utilizing bulk sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkMerge<T>(IEnumerable<T> newRecords)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for syncing</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkUpdate_" data-uid="EFBox.BulkOperations.BulkUpdate*"></a>
  <h4 id="EFBox_BulkOperations_BulkUpdate__1_IEnumerable___0__Action_EFBox_BulkOptions___0___" data-uid="EFBox.BulkOperations.BulkUpdate``1(IEnumerable{``0},Action{EFBox.BulkOptions{``0}})">BulkUpdate&lt;T&gt;(IEnumerable&lt;T&gt;, Action&lt;BulkOptions&lt;T&gt;&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you update a large number of records in your database by utilizing bulk update sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkUpdate<T>(IEnumerable<T> newRecords, Action<BulkOptions<T>> options)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for updating</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOperations_BulkUpdate_" data-uid="EFBox.BulkOperations.BulkUpdate*"></a>
  <h4 id="EFBox_BulkOperations_BulkUpdate__1_IEnumerable___0__" data-uid="EFBox.BulkOperations.BulkUpdate``1(IEnumerable{``0})">BulkUpdate&lt;T&gt;(IEnumerable&lt;T&gt;)</h4>
  <div class="markdown level1 summary"><p>Let you update a large number of records in your database by utilizing bulk update sql</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public void BulkUpdate<T>(IEnumerable<T> newRecords)
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
        <td><span class="xref">IEnumerable&lt;&gt;</span>&lt;T&gt;</td>
        <td><span class="parametername">newRecords</span></td>
        <td><p>List containing the records for updating</p>
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
        <td><p>Data type used for the bulk operation</p>
</td>
      </tr>
    </tbody>
  </table>

{{< /rawhtml >}}
