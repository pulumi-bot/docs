---
title: Module analysisservices
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../">@pulumi/azure</a> &gt; analysisservices

> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-azurerm)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-azure` repo](https://github.com/pulumi/pulumi-azure/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-azurerm` repo](https://github.com/terraform-providers/terraform-provider-azurerm/issues).



<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#Server">class Server</a></li>
<li><a href="#ServerArgs">interface ServerArgs</a></li>
<li><a href="#ServerState">interface ServerState</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts">analysisservices/server.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="Server">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L42">class <b>Server</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

Manages an Analysis Services Server.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const rg = new azure.core.ResourceGroup("rg", {
    location: "northeurope",
    name: "analysis-services-server-test",
});
const server = new azure.analysisservices.Server("server", {
    adminUsers: ["myuser@domain.tld"],
    enablePowerBiService: true,
    ipv4FirewallRules: [{
        name: "myRule1",
        rangeEnd: "210.117.252.255",
        rangeStart: "210.117.252.0",
    }],
    location: "northeurope",
    name: "analysisservicesserver",
    resourceGroupName: rg.name,
    sku: "S0",
    tags: {
        abc: 123,
    },
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/analysis_services_server.html.markdown.

{{% /md %}}
<h3 class="pdoc-member-header" id="Server-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L101"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Server(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#ServerArgs'>ServerArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>

{{% md %}}

Create a Server resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L51">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#ServerState'>ServerState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Server'>Server</a></pre>

{{% md %}}

Get an existing Server resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L42">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L62">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>

{{% md %}}

Returns true if the given object is an instance of Server.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-adminUsers">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L72">property <b>adminUsers</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>adminUsers: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

List of email addresses of admin users.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-enablePowerBiService">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L76">property <b>enablePowerBiService</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>enablePowerBiService: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

Indicates if the Power BI service is allowed to access or not.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L42">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-ipv4FirewallRules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L80">property <b>ipv4FirewallRules</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>ipv4FirewallRules: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<a href='#ServerIpv4FirewallRule'>ServerIpv4FirewallRule</a>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

One or more `ipv4FirewallRule` block(s) as defined below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L84">property <b>location</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>location: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The Azure location where the Analysis Services Server exists. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L88">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Specifies the name of the firewall rule.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-querypoolConnectionMode">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L92">property <b>querypoolConnectionMode</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>querypoolConnectionMode: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Controls how the read-write server is used in the query pool. If this values is set to `All` then read-write servers are also used for queries. Otherwise with `ReadOnly` these servers do not participate in query operations.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L96">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Resource Group in which the Analysis Services Server should be exist. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-sku">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L100">property <b>sku</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>sku: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

SKU for the Analysis Services Server. Possible values are: `D1`, `B1`, `B2`, `S0`, `S1`, `S2`, `S4`, `S8` and `S9`

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Server-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L101">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>tags: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>}&gt;;</pre>
</div>
<h3 class="pdoc-member-header" id="Server-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L42">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="ServerArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L195">interface <b>ServerArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

The set of arguments for constructing a Server resource.

{{% /md %}}
<h3 class="pdoc-member-header" id="ServerArgs-adminUsers">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L199">property <b>adminUsers</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>adminUsers?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

List of email addresses of admin users.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-enablePowerBiService">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L203">property <b>enablePowerBiService</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>enablePowerBiService?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</pre>
{{% md %}}

Indicates if the Power BI service is allowed to access or not.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-ipv4FirewallRules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L207">property <b>ipv4FirewallRules</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>ipv4FirewallRules?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='#ServerIpv4FirewallRule'>ServerIpv4FirewallRule</a>&gt;[]&gt;;</pre>
{{% md %}}

One or more `ipv4FirewallRule` block(s) as defined below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L211">property <b>location</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>location?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The Azure location where the Analysis Services Server exists. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L215">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Specifies the name of the firewall rule.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-querypoolConnectionMode">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L219">property <b>querypoolConnectionMode</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>querypoolConnectionMode?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Controls how the read-write server is used in the query pool. If this values is set to `All` then read-write servers are also used for queries. Otherwise with `ReadOnly` these servers do not participate in query operations.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L223">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>resourceGroupName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Resource Group in which the Analysis Services Server should be exist. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-sku">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L227">property <b>sku</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>sku: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

SKU for the Analysis Services Server. Possible values are: `D1`, `B1`, `B2`, `S0`, `S1`, `S2`, `S4`, `S8` and `S9`

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerArgs-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L228">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>}&gt;;</pre>
</div>
</div>
<h2 class="pdoc-module-header" id="ServerState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L156">interface <b>ServerState</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

Input properties used for looking up and filtering Server resources.

{{% /md %}}
<h3 class="pdoc-member-header" id="ServerState-adminUsers">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L160">property <b>adminUsers</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>adminUsers?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

List of email addresses of admin users.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-enablePowerBiService">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L164">property <b>enablePowerBiService</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>enablePowerBiService?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>&gt;;</pre>
{{% md %}}

Indicates if the Power BI service is allowed to access or not.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-ipv4FirewallRules">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L168">property <b>ipv4FirewallRules</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>ipv4FirewallRules?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='#ServerIpv4FirewallRule'>ServerIpv4FirewallRule</a>&gt;[]&gt;;</pre>
{{% md %}}

One or more `ipv4FirewallRule` block(s) as defined below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-location">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L172">property <b>location</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>location?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The Azure location where the Analysis Services Server exists. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L176">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Specifies the name of the firewall rule.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-querypoolConnectionMode">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L180">property <b>querypoolConnectionMode</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>querypoolConnectionMode?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Controls how the read-write server is used in the query pool. If this values is set to `All` then read-write servers are also used for queries. Otherwise with `ReadOnly` these servers do not participate in query operations.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-resourceGroupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L184">property <b>resourceGroupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>resourceGroupName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Resource Group in which the Analysis Services Server should be exist. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-sku">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L188">property <b>sku</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>sku?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

SKU for the Analysis Services Server. Possible values are: `D1`, `B1`, `B2`, `S0`, `S1`, `S2`, `S4`, `S8` and `S9`

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ServerState-tags">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/18ca42dc2b387b1266e070d028c8c5387e463b92/sdk/nodejs/analysisservices/server.ts#L189">property <b>tags</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>tags?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{[key: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>]: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>}&gt;;</pre>
</div>
</div>
