---
title: Module types/input
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../../">@pulumi/gitlab</a> &gt; <a href="../">types</a> &gt; input

<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#ProjectSharedWithGroup">interface ProjectSharedWithGroup</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-gitlab/blob/028b061a7ff4237d00706de80d79c333ab5cf8eb/sdk/nodejs/types/input.ts">types/input.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="ProjectSharedWithGroup">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gitlab/blob/028b061a7ff4237d00706de80d79c333ab5cf8eb/sdk/nodejs/types/input.ts#L7">interface <b>ProjectSharedWithGroup</b></a>
</h2>
<div class="pdoc-module-contents">
<h3 class="pdoc-member-header" id="ProjectSharedWithGroup-groupAccessLevel">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gitlab/blob/028b061a7ff4237d00706de80d79c333ab5cf8eb/sdk/nodejs/types/input.ts#L12">property <b>groupAccessLevel</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupAccessLevel: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Group's sharing permissions. See [group members permission][groupMembersPermissions] for more info.
Valid values are `guest`, `reporter`, `developer`, `master`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ProjectSharedWithGroup-groupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gitlab/blob/028b061a7ff4237d00706de80d79c333ab5cf8eb/sdk/nodejs/types/input.ts#L16">property <b>groupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;</pre>
{{% md %}}

Group id of the group you want to share the project with.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ProjectSharedWithGroup-groupName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gitlab/blob/028b061a7ff4237d00706de80d79c333ab5cf8eb/sdk/nodejs/types/input.ts#L20">property <b>groupName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

Group's name.

{{% /md %}}
</div>
</div>
