---
title: Module apiregistration/v1
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../../">@pulumi/kubernetes</a> &gt; <a href="../">apiregistration</a> &gt; v1

<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#APIService">class APIService</a></li>
<li><a href="#APIServiceList">class APIServiceList</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts">apiregistration/v1/APIService.ts</a> <a href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts">apiregistration/v1/APIServiceList.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="APIService">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L13">class <b>APIService</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

APIService represents a server for a particular GroupVersion. Name must be "version.group".

{{% /md %}}
<h3 class="pdoc-member-header" id="APIService-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L71"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> APIService(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args?: <a href='/docs/reference/pkg/nodejs/pulumi/kubernetes/types/input/#APIService'>inputs.apiregistration.v1.APIService</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a apiregistration.v1.APIService resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L54">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#APIService'>APIService</a></pre>

{{% md %}}

Get the state of an existing `APIService` resource, as identified by `id`.
The ID is of the form `[namespace]/&lt;name&gt;`; if `namespace` is omitted, then (per
Kubernetes convention) the ID becomes `default/&lt;name&gt;`.

Pulumi will keep track of this resource using `name` as the Pulumi ID.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L13">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L65">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of APIService.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-apiVersion">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L20">property <b>apiVersion</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>apiVersion: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"apiregistration.k8s.io/v1"</span>&gt;;</pre>
{{% md %}}

APIVersion defines the versioned schema of this representation of an object. Servers should
convert recognized schemas to the latest internal value, and may reject unrecognized
values. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L13">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L28">property <b>kind</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>kind: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"APIService"</span>&gt;;</pre>
{{% md %}}

Kind is a string value representing the REST resource this object represents. Servers may
infer this from the endpoint the client submits requests to. Cannot be updated. In
CamelCase. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-metadata">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L31">property <b>metadata</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>metadata: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ObjectMeta'>ObjectMeta</a>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="APIService-spec">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L36">property <b>spec</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>spec: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#APIServiceSpec'>APIServiceSpec</a>&gt;;</pre>
{{% md %}}

Spec contains information for locating and communicating with a server

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-status">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L41">property <b>status</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>status: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#APIServiceStatus'>APIServiceStatus</a>&gt;;</pre>
{{% md %}}

Status contains derived information about an API server

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIService-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIService.ts#L13">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="APIServiceList">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L13">class <b>APIServiceList</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

APIServiceList is a list of APIService objects.

{{% /md %}}
<h3 class="pdoc-member-header" id="APIServiceList-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L64"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> APIServiceList(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args?: <a href='/docs/reference/pkg/nodejs/pulumi/kubernetes/types/input/#APIServiceList'>inputs.apiregistration.v1.APIServiceList</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a apiregistration.v1.APIServiceList resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L47">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#APIServiceList'>APIServiceList</a></pre>

{{% md %}}

Get the state of an existing `APIServiceList` resource, as identified by `id`.
The ID is of the form `[namespace]/&lt;name&gt;`; if `namespace` is omitted, then (per
Kubernetes convention) the ID becomes `default/&lt;name&gt;`.

Pulumi will keep track of this resource using `name` as the Pulumi ID.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L13">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L58">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of APIServiceList.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-apiVersion">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L20">property <b>apiVersion</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>apiVersion: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"apiregistration.k8s.io/v1"</span>&gt;;</pre>
{{% md %}}

APIVersion defines the versioned schema of this representation of an object. Servers should
convert recognized schemas to the latest internal value, and may reject unrecognized
values. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L13">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-items">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L23">property <b>items</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>items: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#APIService'>APIService</a>[]&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="APIServiceList-kind">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L31">property <b>kind</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>kind: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='s2'>"APIServiceList"</span>&gt;;</pre>
{{% md %}}

Kind is a string value representing the REST resource this object represents. Servers may
infer this from the endpoint the client submits requests to. Cannot be updated. In
CamelCase. More info:
https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="APIServiceList-metadata">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L34">property <b>metadata</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>metadata: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ListMeta'>ListMeta</a>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="APIServiceList-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-kubernetes/blob/491e0cf7ac2d4f43c3337af41a0f918cab31eb25/sdk/nodejs/apiregistration/v1/APIServiceList.ts#L13">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
