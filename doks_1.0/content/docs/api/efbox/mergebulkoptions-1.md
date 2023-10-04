---
title: "MergeBulkOptions<T>"
description: "Details for Class MergeBulkOptions<T> (EFBox)"
draft: false
images: []
menu:
  api:
    parent: "efbox"
weight: 10003
toc: false
---

{{< rawhtml >}}

            <article class="content wrap" id="_content" data-uid="EFBox.MergeBulkOptions`1">
  <h1 id="EFBox_MergeBulkOptions_1" data-uid="EFBox.MergeBulkOptions`1" class="text-break">Class MergeBulkOptions&lt;T&gt;
</h1>
  <div class="markdown level0 summary"><p>Options used for BulkMerge operations.</p>
</div>
  <div class="markdown level0 conceptual"></div>
  <div class="inheritance">
    <h5>Inheritance</h5>
    <div class="level0"><span class="xref">System.Object</span></div>
    <div class="level1"><a class="xref" href="/docs/api/efbox/bulkoptionsshared-1">BulkOptionsShared</a>&lt;T&gt;</div>
    <div class="level2"><span class="xref">MergeBulkOptions&lt;T&gt;</span></div>
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
  <h5 id="EFBox_MergeBulkOptions_1_syntax">Syntax</h5>
{{< /rawhtml >}}

```C#
    public class MergeBulkOptions<T> : BulkOptionsShared<T>
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
  <a id="EFBox_MergeBulkOptions_1_CacheMode_" data-uid="EFBox.MergeBulkOptions`1.CacheMode*"></a>
  <h4 id="EFBox_MergeBulkOptions_1_CacheMode" data-uid="EFBox.MergeBulkOptions`1.CacheMode">CacheMode</h4>
  <div class="markdown level1 summary"><p>Determines the cache mode. Default is <span class="xref">ETLBox.CacheMode.Full</span>.
If set to <span class="xref">ETLBox.CacheMode.Partial</span>, only data that is needed to process the current batch
is loaded from the destination table. This will slow down execution performance,
but memory consumption may decrease.
If <a class="xref" href="/docs/api/efbox/mergebulkoptions-1#EFBox_MergeBulkOptions_1_MergeMode">MergeMode</a> is set to <span class="xref">ETLBox.MergeMode.Full</span>, this setting is ignored
(<span class="xref">ETLBox.CacheMode.Full</span> is used)</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public CacheMode CacheMode { get; set; }
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
        <td><span class="xref">ETLBox.CacheMode</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_MergeBulkOptions_1_CompareColumns_" data-uid="EFBox.MergeBulkOptions`1.CompareColumns*"></a>
  <h4 id="EFBox_MergeBulkOptions_1_CompareColumns" data-uid="EFBox.MergeBulkOptions`1.CompareColumns">CompareColumns</h4>
  <div class="markdown level1 summary"><p>Define properties to check for equality during merge to decide
if an update is needed.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public ICollection<CompareColumn> CompareColumns { get; set; }
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
        <td><span class="xref">ICollection&lt;&gt;</span>&lt;<span class="xref">CompareColumn</span>&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_MergeBulkOptions_1_DeleteColumns_" data-uid="EFBox.MergeBulkOptions`1.DeleteColumns*"></a>
  <h4 id="EFBox_MergeBulkOptions_1_DeleteColumns" data-uid="EFBox.MergeBulkOptions`1.DeleteColumns">DeleteColumns</h4>
  <div class="markdown level1 summary"><p>List property names along with a specific value indicating if a row is eligible for deletion during the merge operation.
This option provides a way to mark rows for deletion based on certain criteria.
Only applies if <a class="xref" href="/docs/api/efbox/mergebulkoptions-1#EFBox_MergeBulkOptions_1_MergeMode">MergeMode</a> is set to <span class="xref">ETLBox.MergeMode.Delta</span>.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public ICollection<DeleteColumn> DeleteColumns { get; set; }
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
        <td><span class="xref">ICollection&lt;&gt;</span>&lt;<span class="xref">DeleteColumn</span>&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_MergeBulkOptions_1_FindDuplicates_" data-uid="EFBox.MergeBulkOptions`1.FindDuplicates*"></a>
  <h4 id="EFBox_MergeBulkOptions_1_FindDuplicates" data-uid="EFBox.MergeBulkOptions`1.FindDuplicates">FindDuplicates</h4>
  <div class="markdown level1 summary"><p>Indicates whether to look for duplicate records</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public bool FindDuplicates { get; set; }
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
  <a id="EFBox_MergeBulkOptions_1_MergeMode_" data-uid="EFBox.MergeBulkOptions`1.MergeMode*"></a>
  <h4 id="EFBox_MergeBulkOptions_1_MergeMode" data-uid="EFBox.MergeBulkOptions`1.MergeMode">MergeMode</h4>
  <div class="markdown level1 summary"><p>Specifies the merge mode. Default is <span class="xref">ETLBox.MergeMode.Full</span>.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public MergeMode MergeMode { get; set; }
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
        <td><span class="xref">ETLBox.MergeMode</span></td>
        <td></td>
      </tr>
    </tbody>
  </table>
  <a id="EFBox_MergeBulkOptions_1_UpdateColumns_" data-uid="EFBox.MergeBulkOptions`1.UpdateColumns*"></a>
  <h4 id="EFBox_MergeBulkOptions_1_UpdateColumns" data-uid="EFBox.MergeBulkOptions`1.UpdateColumns">UpdateColumns</h4>
  <div class="markdown level1 summary"><p>Specify properties to be updated when a row needs updating,
by default all non-ID columns are updated.</p>
</div>
  <div class="markdown level1 conceptual"></div>
  <h5 class="declaration">Declaration</h5>
{{< /rawhtml >}}

```C#
    public ICollection<UpdateColumn> UpdateColumns { get; set; }
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
        <td><span class="xref">ICollection&lt;&gt;</span>&lt;<span class="xref">UpdateColumn</span>&gt;</td>
        <td></td>
      </tr>
    </tbody>
  </table>

{{< /rawhtml >}}
