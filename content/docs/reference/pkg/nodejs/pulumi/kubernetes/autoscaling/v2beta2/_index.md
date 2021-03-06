---
title: Module autoscaling/v2beta2
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../../">@pulumi/kubernetes</a> &gt; <a href="../">autoscaling</a> &gt; v2beta2

<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#HorizontalPodAutoscaler">class HorizontalPodAutoscaler</a></li>
<li><a href="#HorizontalPodAutoscalerList">class HorizontalPodAutoscalerList</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts">autoscaling/v2beta2/HorizontalPodAutoscaler.ts</a> <a href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts">autoscaling/v2beta2/HorizontalPodAutoscalerList.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="HorizontalPodAutoscaler">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L15">class <b>HorizontalPodAutoscaler</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

HorizontalPodAutoscaler is the configuration for a horizontal pod autoscaler, which
automatically manages the replica count of any resource implementing the scale subresource
based on the metrics specified.

{{% /md %}}
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L77"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> HorizontalPodAutoscaler(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args?: <a href='/docs/reference/pkg/nodejs/pulumi/kubernetes/types/input/#HorizontalPodAutoscaler'>inputs.autoscaling.v2beta2.HorizontalPodAutoscaler</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a autoscaling.v2beta2.HorizontalPodAutoscaler resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L60">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#HorizontalPodAutoscaler'>HorizontalPodAutoscaler</a></pre>

{{% md %}}

Get the state of an existing `HorizontalPodAutoscaler` resource, as identified by `id`.
The ID is of the form `[namespace]/&lt;name&gt;`; if `namespace` is omitted, then (per
Kubernetes convention) the ID becomes `default/&lt;name&gt;`.

Pulumi will keep track of this resource using `name` as the Pulumi ID.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L15">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L71">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of HorizontalPodAutoscaler.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-apiVersion">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L22">property <b>apiVersion</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>apiVersion: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"autoscaling/v2beta2"</span>&gt;;</pre>
{{% md %}}

APIVersion defines the versioned schema of this representation of an object. Servers should
convert recognized schemas to the latest internal value, and may reject unrecognized
values. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L15">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L30">property <b>kind</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>kind: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"HorizontalPodAutoscaler"</span>&gt;;</pre>
{{% md %}}

Kind is a string value representing the REST resource this object represents. Servers may
infer this from the endpoint the client submits requests to. Cannot be updated. In
CamelCase. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-metadata">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L36">property <b>metadata</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>metadata: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ObjectMeta'>ObjectMeta</a>&gt;;</pre>
{{% md %}}

metadata is the standard object metadata. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#metadata

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-spec">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L42">property <b>spec</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>spec: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#HorizontalPodAutoscalerSpec'>HorizontalPodAutoscalerSpec</a>&gt;;</pre>
{{% md %}}

spec is the specification for the behaviour of the autoscaler. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#spec-and-status.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-status">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L47">property <b>status</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>status: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#HorizontalPodAutoscalerStatus'>HorizontalPodAutoscalerStatus</a>&gt;;</pre>
{{% md %}}

status is the current information about the autoscaler.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscaler-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscaler.ts#L15">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="HorizontalPodAutoscalerList">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L13">class <b>HorizontalPodAutoscalerList</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

HorizontalPodAutoscalerList is a list of horizontal pod autoscaler objects.

{{% /md %}}
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L68"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> HorizontalPodAutoscalerList(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args?: <a href='/docs/reference/pkg/nodejs/pulumi/kubernetes/types/input/#HorizontalPodAutoscalerList'>inputs.autoscaling.v2beta2.HorizontalPodAutoscalerList</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a autoscaling.v2beta2.HorizontalPodAutoscalerList resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L51">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#HorizontalPodAutoscalerList'>HorizontalPodAutoscalerList</a></pre>

{{% md %}}

Get the state of an existing `HorizontalPodAutoscalerList` resource, as identified by `id`.
The ID is of the form `[namespace]/&lt;name&gt;`; if `namespace` is omitted, then (per
Kubernetes convention) the ID becomes `default/&lt;name&gt;`.

Pulumi will keep track of this resource using `name` as the Pulumi ID.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L13">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L62">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of HorizontalPodAutoscalerList.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-apiVersion">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L20">property <b>apiVersion</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>apiVersion: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"autoscaling/v2beta2"</span>&gt;;</pre>
{{% md %}}

APIVersion defines the versioned schema of this representation of an object. Servers should
convert recognized schemas to the latest internal value, and may reject unrecognized
values. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L13">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-items">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L25">property <b>items</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>items: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#HorizontalPodAutoscaler'>HorizontalPodAutoscaler</a>[]&gt;;</pre>
{{% md %}}

items is the list of horizontal pod autoscaler objects.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L33">property <b>kind</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>kind: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"HorizontalPodAutoscalerList"</span>&gt;;</pre>
{{% md %}}

Kind is a string value representing the REST resource this object represents. Servers may
infer this from the endpoint the client submits requests to. Cannot be updated. In
CamelCase. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-metadata">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L38">property <b>metadata</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>metadata: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ListMeta'>ListMeta</a>&gt;;</pre>
{{% md %}}

metadata is the standard list metadata.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="HorizontalPodAutoscalerList-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/autoscaling/v2beta2/HorizontalPodAutoscalerList.ts#L13">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
