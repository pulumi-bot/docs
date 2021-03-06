---
title: Module endpoints
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../">@pulumi/gcp</a> &gt; endpoints

> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-google)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-gcp` repo](https://github.com/pulumi/pulumi-gcp/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-google` repo](https://github.com/terraform-providers/terraform-provider-google/issues).



<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#Service">class Service</a></li>
<li><a href="#ServiceArgs">interface ServiceArgs</a></li>
<li><a href="#ServiceState">interface ServiceState</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts">endpoints/service.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="Service">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L36">class <b>Service</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

This resource creates and rolls out a Cloud Endpoints service using OpenAPI or gRPC.  View the relevant docs for [OpenAPI](https://cloud.google.com/endpoints/docs/openapi/) and [gRPC](https://cloud.google.com/endpoints/docs/grpc/).

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as fs from "fs";
import * as gcp from "@pulumi/gcp";

const grpcService = new gcp.endpoints.Service("grpcService", {
    grpcConfig: fs.readFileSync("service_spec.yml", "utf-8"),
    project: "project-id",
    protocOutputBase64: Buffer.from(fs.readFileSync("compiled_descriptor_file.pb", "utf-8")).toString("base64"),
    serviceName: "api-name.endpoints.project-id.cloud.goog",
});
const openapiService = new gcp.endpoints.Service("openapiService", {
    openapiConfig: fs.readFileSync("openapi_spec.yml", "utf-8"),
    project: "project-id",
    serviceName: "api-name.endpoints.project-id.cloud.goog",
});
```

The example in `examples/endpoints_on_compute_engine` shows the API from the quickstart running on a Compute Engine VM and reachable through Cloud Endpoints, which may also be useful.

> This content is derived from https://github.com/terraform-providers/terraform-provider-google/blob/master/website/docs/r/endpoints_service.html.markdown.

{{% /md %}}
<h3 class="pdoc-member-header" id="Service-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L71"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Service(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#ServiceArgs'>ServiceArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a Service resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Service-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L45">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#ServiceState'>ServiceState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Service'>Service</a></pre>

{{% md %}}

Get an existing Service resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Service-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L36">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Service-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L56">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of Service.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Service-apis">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L63">property <b>apis</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>apis: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ServiceApi'>ServiceApi</a>[]&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-configId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L64">property <b>configId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>configId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-dnsAddress">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L65">property <b>dnsAddress</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>dnsAddress: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-endpoints">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L66">property <b>endpoints</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>endpoints: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ServiceEndpoint'>ServiceEndpoint</a>[]&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-grpcConfig">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L67">property <b>grpcConfig</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>grpcConfig: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L36">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Service-openapiConfig">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L68">property <b>openapiConfig</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>openapiConfig: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L69">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>project: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-protocOutputBase64">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L70">property <b>protocOutputBase64</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>protocOutputBase64: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-serviceName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L71">property <b>serviceName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>serviceName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Service-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L36">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="ServiceArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L138">interface <b>ServiceArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

The set of arguments for constructing a Service resource.

{{% /md %}}
<h3 class="pdoc-member-header" id="ServiceArgs-grpcConfig">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L139">property <b>grpcConfig</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>grpcConfig?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceArgs-openapiConfig">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L140">property <b>openapiConfig</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>openapiConfig?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceArgs-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L141">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>project?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceArgs-protocOutputBase64">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L142">property <b>protocOutputBase64</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>protocOutputBase64?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceArgs-serviceName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L143">property <b>serviceName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>serviceName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
</div>
<h2 class="pdoc-module-header" id="ServiceState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L123">interface <b>ServiceState</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

Input properties used for looking up and filtering Service resources.

{{% /md %}}
<h3 class="pdoc-member-header" id="ServiceState-apis">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L124">property <b>apis</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>apis?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='#ServiceApi'>ServiceApi</a>&gt;[]&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-configId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L125">property <b>configId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>configId?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-dnsAddress">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L126">property <b>dnsAddress</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>dnsAddress?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-endpoints">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L127">property <b>endpoints</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>endpoints?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='#ServiceEndpoint'>ServiceEndpoint</a>&gt;[]&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-grpcConfig">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L128">property <b>grpcConfig</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>grpcConfig?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-openapiConfig">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L129">property <b>openapiConfig</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>openapiConfig?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L130">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>project?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-protocOutputBase64">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L131">property <b>protocOutputBase64</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>protocOutputBase64?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="ServiceState-serviceName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/9241c1cc472b05b656d64f1c3022a8eb88aeebbe/sdk/nodejs/endpoints/service.ts#L132">property <b>serviceName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>serviceName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
</div>
</div>
