---
title: Module types/output
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../../">@pulumi/packet</a> &gt; <a href="../">types</a> &gt; output

<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#DeviceNetwork">interface DeviceNetwork</a></li>
<li><a href="#DevicePort">interface DevicePort</a></li>
<li><a href="#ProjectBgpConfig">interface ProjectBgpConfig</a></li>
<li><a href="#SpotMarketRequestInstanceParameters">interface SpotMarketRequestInstanceParameters</a></li>
<li><a href="#VolumeAttachment">interface VolumeAttachment</a></li>
<li><a href="#VolumeSnapshotPolicy">interface VolumeSnapshotPolicy</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts">types/output.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="DeviceNetwork">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L7">interface <b>DeviceNetwork</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="DeviceNetwork-address">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L11">property <b>address</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>address: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

IPv4 or IPv6 address string

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DeviceNetwork-cidr">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L15">property <b>cidr</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>cidr: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>;</pre>
{{% md %}}

bit length of the network mask of the address

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DeviceNetwork-family">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L19">property <b>family</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>family: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>;</pre>
{{% md %}}

IP version - "4" or "6"

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DeviceNetwork-gateway">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L23">property <b>gateway</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>gateway: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

address of router

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DeviceNetwork-public">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L27">property <b>public</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>public: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>;</pre>
{{% md %}}

whether the address is routable from the Internet

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="DevicePort">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L30">interface <b>DevicePort</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="DevicePort-bonded">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L35">property <b>bonded</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>bonded: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span>;</pre>
{{% md %}}

Whether this port is part of a bond in bonded network setup
* `projectId`- The ID of the project the device belongs to

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DevicePort-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L39">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

ID of the port

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DevicePort-mac">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L43">property <b>mac</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>mac: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

MAC address assigned to the port

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DevicePort-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L47">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

Name of the port (e.g. `eth0`, or `bond0`)

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="DevicePort-type">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L51">property <b>type</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>type: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

Type of the port (e.g. `NetworkPort` or `NetworkBondPort`)

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="ProjectBgpConfig">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L54">interface <b>ProjectBgpConfig</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="ProjectBgpConfig-asn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L55">property <b>asn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>asn: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="ProjectBgpConfig-deploymentType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L56">property <b>deploymentType</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>deploymentType: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="ProjectBgpConfig-maxPrefix">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L60">property <b>maxPrefix</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>maxPrefix: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>;</pre>
{{% md %}}

The maximum number of route filters allowed per server

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ProjectBgpConfig-md5">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L61">property <b>md5</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>md5?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="ProjectBgpConfig-status">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L65">property <b>status</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>status: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

status of BGP configuration in the project

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="SpotMarketRequestInstanceParameters">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L68">interface <b>SpotMarketRequestInstanceParameters</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-alwaysPxe">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L69">property <b>alwaysPxe</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>alwaysPxe?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-billingCycle">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L70">property <b>billingCycle</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>billingCycle: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-description">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L71">property <b>description</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>description?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-features">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L72">property <b>features</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>features?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-hostname">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L73">property <b>hostname</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>hostname: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-locked">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L74">property <b>locked</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>locked?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-operatingSystem">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L75">property <b>operatingSystem</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>operatingSystem: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-plan">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L76">property <b>plan</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>plan: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-projectSshKeys">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L77">property <b>projectSshKeys</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>projectSshKeys?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-termintationTime">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L78">property <b>termintationTime</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>termintationTime: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-userSshKeys">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L79">property <b>userSshKeys</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>userSshKeys?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</pre>
</div>
<h3 class="pdoc-member-header" id="SpotMarketRequestInstanceParameters-userdata">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L80">property <b>userdata</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>userdata?: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
</div>
<h2 class="pdoc-module-header" id="VolumeAttachment">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L83">interface <b>VolumeAttachment</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="VolumeAttachment-href">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L84">property <b>href</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>href: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
</div>
<h2 class="pdoc-module-header" id="VolumeSnapshotPolicy">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L87">interface <b>VolumeSnapshotPolicy</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="VolumeSnapshotPolicy-snapshotCount">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L88">property <b>snapshotCount</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>snapshotCount: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>;</pre>
</div>
<h3 class="pdoc-member-header" id="VolumeSnapshotPolicy-snapshotFrequency">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-packet/blob/bb2af53671d3406aeb9a2bc112acfb38862d2ae0/sdk/nodejs/types/output.ts#L89">property <b>snapshotFrequency</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>snapshotFrequency: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
</div>
</div>
