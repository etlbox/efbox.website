---
title: "BulkOptionsShared<T>"
description: "Details for Class BulkOptionsShared<T> (EFBox)"
draft: false
images: []
menu:
  api:
    parent: "efbox"
weight: 10002
toc: false
---

{{< rawhtml >}}

            <article class="content wrap" id="_content" data-uid="EFBox.BulkOptionsShared`1">
  <h1 id="EFBox_BulkOptionsShared_1" data-uid="EFBox.BulkOptionsShared`1" class="text-break">Class BulkOptionsShared&lt;T&gt;
</h1>
  <div class="markdown level0 summary"></div>
  <div class="markdown level0 conceptual"></div>
  <div class="inheritance">
    <h5>Inheritance</h5>
    <div class="level0"><span class="xref">System.Object</span></div>
    <div class="level1"><span class="xref">BulkOptionsShared&lt;T&gt;</span></div>
      <div class="level2"><a class="xref" href="/docs/api/efbox/bulkoptions-1">BulkOptions&lt;T&gt;</a></div>
      <div class="level2"><a class="xref" href="/docs/api/efbox/mergebulkoptions-1">MergeBulkOptions&lt;T&gt;</a></div>
  </div>
<h6><strong>Namespace</strong>: EFBox</h6>
  <h6><strong>Assembly</strong>: EFBox.dll</h6>
  <h5 id="EFBox_BulkOptionsShared_1_syntax">Syntax</h5>
{{< /rawhtml >}}

```C#
    public abstract class BulkOptionsShared<T>
```

{{< rawhtml >}}
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
        <td></td>
      </tr>
    </tbody>
  </table>
  <h3 id="properties">Properties
</h3>
  <a id="EFBox_BulkOptionsShared_1_AllowIdentityInsert_" data-uid="EFBox.BulkOptionsShared`1.AllowIdentityInsert*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_AllowIdentityInsert" data-uid="EFBox.BulkOptionsShared`1.AllowIdentityInsert">AllowIdentityInsert</h4>
  <div class="markdown level1 summary"><p>Enables identity insert for the operation - this will override
existing values in identity / auto-increment / serial columns.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public bool AllowIdentityInsert { get; set; }
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
        <td><span class="xref">bool</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptionsShared_1_BatchSize_" data-uid="EFBox.BulkOptionsShared`1.BatchSize*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_BatchSize" data-uid="EFBox.BulkOptionsShared`1.BatchSize">BatchSize</h4>
  <div class="markdown level1 summary"><p>The number of records to be processed in a single batch.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public int BatchSize { get; set; }
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
        <td><span class="xref">int</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptionsShared_1_ColumnConverters_" data-uid="EFBox.BulkOptionsShared`1.ColumnConverters*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_ColumnConverters" data-uid="EFBox.BulkOptionsShared`1.ColumnConverters">ColumnConverters</h4>
  <div class="markdown level1 summary"><p>Allows custom conversions for specific columns.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public ICollection<ColumnConverter> ColumnConverters { get; set; }
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
        <td><span class="xref">ICollection&lt;&gt;</span>&lt;<span class="xref">ColumnConverter</span>&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptionsShared_1_ErrorData_" data-uid="EFBox.BulkOptionsShared`1.ErrorData*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_ErrorData" data-uid="EFBox.BulkOptionsShared`1.ErrorData">ErrorData</h4>
  <div class="markdown level1 summary"><p>Contains erroneous data.
<a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_RedirectErroneousBatches">RedirectErroneousBatches</a> must be set to true.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public ICollection<ETLBoxError> ErrorData { get; set; }
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
        <td><span class="xref">ICollection&lt;&gt;</span>&lt;<span class="xref">ETLBoxError</span>&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptionsShared_1_OnProgress_" data-uid="EFBox.BulkOptionsShared`1.OnProgress*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_OnProgress" data-uid="EFBox.BulkOptionsShared`1.OnProgress">OnProgress</h4>
  <div class="markdown level1 summary"><p>Action is invoked for every processed batch.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public Action<int> OnProgress { get; set; }
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
        <td><span class="xref">Action&lt;&gt;</span>&lt;<span class="xref">int</span>&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptionsShared_1_ReadGeneratedValues_" data-uid="EFBox.BulkOptionsShared`1.ReadGeneratedValues*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_ReadGeneratedValues" data-uid="EFBox.BulkOptionsShared`1.ReadGeneratedValues">ReadGeneratedValues</h4>
  <div class="markdown level1 summary"><p>Indicates whether to read back generated values like auto-incremented IDs.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public bool ReadGeneratedValues { get; set; }
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
        <td><span class="xref">bool</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptionsShared_1_RedirectErroneousBatches_" data-uid="EFBox.BulkOptionsShared`1.RedirectErroneousBatches*"></a>
  <h4 id="EFBox_BulkOptionsShared_1_RedirectErroneousBatches" data-uid="EFBox.BulkOptionsShared`1.RedirectErroneousBatches">RedirectErroneousBatches</h4>
  <div class="markdown level1 summary"><p>Indicates whether to redirect erroneous batches.<br>
By default an exception is thrown when a batch can't be inserted into a database,
and the bulk operation is stopped.
Setting this to true won't stop execution when a batch can't be processed.
<a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_ErrorData">ErrorData</a> will hold details about flawed batch.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public bool RedirectErroneousBatches { get; set; }
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
        <td><span class="xref">bool</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>

{{< /rawhtml >}}
