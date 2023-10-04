---
title: "BulkOptions<T>"
description: "Details for Class BulkOptions<T> (EFBox)"
draft: false
images: []
menu:
  api:
    parent: "efbox"
weight: 10001
toc: false
---

{{< rawhtml >}}

            <article class="content wrap" id="_content" data-uid="EFBox.BulkOptions`1">
  <h1 id="EFBox_BulkOptions_1" data-uid="EFBox.BulkOptions`1" class="text-break">Class BulkOptions&lt;T&gt;
</h1>
  <div class="markdown level0 summary"><p>Options used for BulkInsert/BulkUpdate/BulkDelete operations.</p>
</div>
  <div class="markdown level0 conceptual"></div>
  <div class="inheritance">
    <h5>Inheritance</h5>
    <div class="level0"><span class="xref">System.Object</span></div>
    <div class="level1"><a class="xref" href="/docs/api/efbox/bulkoptionsshared-1">BulkOptionsShared</a>&lt;T&gt;</div>
    <div class="level2"><span class="xref">BulkOptions&lt;T&gt;</span></div>
  </div>
  <div class="inheritedMembers">
    <h5>Inherited Members</h5>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_BatchSize">BulkOptionsShared&lt;T&gt;.BatchSize</a>
    </div>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_ReadGeneratedValues">BulkOptionsShared&lt;T&gt;.ReadGeneratedValues</a>
    </div>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_ColumnConverters">BulkOptionsShared&lt;T&gt;.ColumnConverters</a>
    </div>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_AllowIdentityInsert">BulkOptionsShared&lt;T&gt;.AllowIdentityInsert</a>
    </div>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_OnProgress">BulkOptionsShared&lt;T&gt;.OnProgress</a>
    </div>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_ErrorData">BulkOptionsShared&lt;T&gt;.ErrorData</a>
    </div>
    <div>
      <a class="xref" href="/docs/api/efbox/bulkoptionsshared-1#EFBox_BulkOptionsShared_1_RedirectErroneousBatches">BulkOptionsShared&lt;T&gt;.RedirectErroneousBatches</a>
    </div>
  </div>
<h6><strong>Namespace</strong>: EFBox</h6>
  <h6><strong>Assembly</strong>: EFBox.dll</h6>
  <h5 id="EFBox_BulkOptions_1_syntax">Syntax</h5>
{{< /rawhtml >}}

```C#
    public class BulkOptions<T> : BulkOptionsShared<T>
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
        <td><p>Type of data used for operation</p>
</td>
      </tr>
    </tbody>
  </table>
  <h3 id="properties">Properties
</h3>
  <a id="EFBox_BulkOptions_1_AfterBatchWrite_" data-uid="EFBox.BulkOptions`1.AfterBatchWrite*"></a>
  <h4 id="EFBox_BulkOptions_1_AfterBatchWrite" data-uid="EFBox.BulkOptions`1.AfterBatchWrite">AfterBatchWrite</h4>
  <div class="markdown level1 summary"><p>Action to perform tasks after batch write.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public Action<T[]> AfterBatchWrite { get; set; }
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
        <td><span class="xref">Action&lt;&gt;</span>&lt;T[]&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_BulkOptions_1_BeforeBatchWrite_" data-uid="EFBox.BulkOptions`1.BeforeBatchWrite*"></a>
  <h4 id="EFBox_BulkOptions_1_BeforeBatchWrite" data-uid="EFBox.BulkOptions`1.BeforeBatchWrite">BeforeBatchWrite</h4>
  <div class="markdown level1 summary"><p>Function to modify data before batch write.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public Func<T[], T[]> BeforeBatchWrite { get; set; }
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
        <td><span class="xref">Func&lt;, &gt;</span>&lt;T[], T[]&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>

{{< /rawhtml >}}
