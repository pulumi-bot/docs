---
title: Module bot
linktitle: bot
notitle: true
---

<div class="section" id="bot">
<h1>bot<a class="headerlink" href="#bot" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-azure/issues">pulumi/pulumi-azure repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/issues">terraform-providers/terraform-provider-azurerm repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_azure.bot"></span><dl class="class">
<dt id="pulumi_azure.bot.ChannelsRegistration">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.bot.</code><code class="sig-name descname">ChannelsRegistration</code><span class="sig-paren">(</span><em class="sig-param">resource_name</em>, <em class="sig-param">opts=None</em>, <em class="sig-param">developer_app_insights_api_key=None</em>, <em class="sig-param">developer_app_insights_application_id=None</em>, <em class="sig-param">developer_app_insights_key=None</em>, <em class="sig-param">display_name=None</em>, <em class="sig-param">endpoint=None</em>, <em class="sig-param">location=None</em>, <em class="sig-param">microsoft_app_id=None</em>, <em class="sig-param">name=None</em>, <em class="sig-param">resource_group_name=None</em>, <em class="sig-param">sku=None</em>, <em class="sig-param">tags=None</em>, <em class="sig-param">__props__=None</em>, <em class="sig-param">__name__=None</em>, <em class="sig-param">__opts__=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages a Bot Channels Registration.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>developer_app_insights_api_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Application Insights API Key to associate with the Bot Channels Registration.</p></li>
<li><p><strong>developer_app_insights_application_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Application Insights Application ID to associate with the Bot Channels Registration.</p></li>
<li><p><strong>developer_app_insights_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Application Insights Key to associate with the Bot Channels Registration.</p></li>
<li><p><strong>display_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Bot Channels Registration will be displayed as. This defaults to <code class="docutils literal notranslate"><span class="pre">name</span></code> if not specified.</p></li>
<li><p><strong>endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Bot Channels Registration endpoint.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>microsoft_app_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Microsoft Application ID for the Bot Channels Registration. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Bot Channels Registration. Changing this forces a new resource to be created. Must be globally unique.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which to create the Bot Channels Registration. Changing this forces a new resource to be created.</p></li>
<li><p><strong>sku</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The SKU of the Bot Channels Registration. Valid values include <code class="docutils literal notranslate"><span class="pre">F0</span></code> or <code class="docutils literal notranslate"><span class="pre">S1</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<blockquote>
<div><p>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_channels_registration.html.markdown">https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_channels_registration.html.markdown</a>.</p>
</div></blockquote>
<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.developer_app_insights_api_key">
<code class="sig-name descname">developer_app_insights_api_key</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.developer_app_insights_api_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Application Insights API Key to associate with the Bot Channels Registration.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.developer_app_insights_application_id">
<code class="sig-name descname">developer_app_insights_application_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.developer_app_insights_application_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The Application Insights Application ID to associate with the Bot Channels Registration.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.developer_app_insights_key">
<code class="sig-name descname">developer_app_insights_key</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.developer_app_insights_key" title="Permalink to this definition">¶</a></dt>
<dd><p>The Application Insights Key to associate with the Bot Channels Registration.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.display_name">
<code class="sig-name descname">display_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.display_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Bot Channels Registration will be displayed as. This defaults to <code class="docutils literal notranslate"><span class="pre">name</span></code> if not specified.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.endpoint">
<code class="sig-name descname">endpoint</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.endpoint" title="Permalink to this definition">¶</a></dt>
<dd><p>The Bot Channels Registration endpoint.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.location">
<code class="sig-name descname">location</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.location" title="Permalink to this definition">¶</a></dt>
<dd><p>The supported Azure location where the resource exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.microsoft_app_id">
<code class="sig-name descname">microsoft_app_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.microsoft_app_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The Microsoft Application ID for the Bot Channels Registration. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.name">
<code class="sig-name descname">name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the Bot Channels Registration. Changing this forces a new resource to be created. Must be globally unique.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the resource group in which to create the Bot Channels Registration. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.sku">
<code class="sig-name descname">sku</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.sku" title="Permalink to this definition">¶</a></dt>
<dd><p>The SKU of the Bot Channels Registration. Valid values include <code class="docutils literal notranslate"><span class="pre">F0</span></code> or <code class="docutils literal notranslate"><span class="pre">S1</span></code>. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.ChannelsRegistration.tags">
<code class="sig-name descname">tags</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_azure.bot.ChannelsRegistration.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param">resource_name</em>, <em class="sig-param">id</em>, <em class="sig-param">opts=None</em>, <em class="sig-param">developer_app_insights_api_key=None</em>, <em class="sig-param">developer_app_insights_application_id=None</em>, <em class="sig-param">developer_app_insights_key=None</em>, <em class="sig-param">display_name=None</em>, <em class="sig-param">endpoint=None</em>, <em class="sig-param">location=None</em>, <em class="sig-param">microsoft_app_id=None</em>, <em class="sig-param">name=None</em>, <em class="sig-param">resource_group_name=None</em>, <em class="sig-param">sku=None</em>, <em class="sig-param">tags=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing ChannelsRegistration resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>developer_app_insights_api_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Application Insights API Key to associate with the Bot Channels Registration.</p></li>
<li><p><strong>developer_app_insights_application_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Application Insights Application ID to associate with the Bot Channels Registration.</p></li>
<li><p><strong>developer_app_insights_key</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Application Insights Key to associate with the Bot Channels Registration.</p></li>
<li><p><strong>display_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Bot Channels Registration will be displayed as. This defaults to <code class="docutils literal notranslate"><span class="pre">name</span></code> if not specified.</p></li>
<li><p><strong>endpoint</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Bot Channels Registration endpoint.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>microsoft_app_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Microsoft Application ID for the Bot Channels Registration. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Bot Channels Registration. Changing this forces a new resource to be created. Must be globally unique.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which to create the Bot Channels Registration. Changing this forces a new resource to be created.</p></li>
<li><p><strong>sku</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The SKU of the Bot Channels Registration. Valid values include <code class="docutils literal notranslate"><span class="pre">F0</span></code> or <code class="docutils literal notranslate"><span class="pre">S1</span></code>. Changing this forces a new resource to be created.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<blockquote>
<div><p>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_channels_registration.html.markdown">https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_channels_registration.html.markdown</a>.</p>
</div></blockquote>
</dd></dl>

<dl class="method">
<dt id="pulumi_azure.bot.ChannelsRegistration.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param">prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="method">
<dt id="pulumi_azure.bot.ChannelsRegistration.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param">prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.ChannelsRegistration.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

<dl class="class">
<dt id="pulumi_azure.bot.Connection">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_azure.bot.</code><code class="sig-name descname">Connection</code><span class="sig-paren">(</span><em class="sig-param">resource_name</em>, <em class="sig-param">opts=None</em>, <em class="sig-param">bot_name=None</em>, <em class="sig-param">client_id=None</em>, <em class="sig-param">client_secret=None</em>, <em class="sig-param">location=None</em>, <em class="sig-param">name=None</em>, <em class="sig-param">parameters=None</em>, <em class="sig-param">resource_group_name=None</em>, <em class="sig-param">scopes=None</em>, <em class="sig-param">service_provider_name=None</em>, <em class="sig-param">tags=None</em>, <em class="sig-param">__props__=None</em>, <em class="sig-param">__name__=None</em>, <em class="sig-param">__opts__=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.Connection" title="Permalink to this definition">¶</a></dt>
<dd><p>Manages a Bot Connection.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>bot_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Bot Resource this connection will be associated with. Changing this forces a new resource to be created.</p></li>
<li><p><strong>client_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Client ID that will be used to authenticate with the service provider.</p></li>
<li><p><strong>client_secret</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Client Secret that will be used to authenticate with the service provider.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Bot Connection. Changing this forces a new resource to be created. Must be globally unique.</p></li>
<li><p><strong>parameters</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A map of additional parameters to apply to the connection.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which to create the Bot Connection. Changing this forces a new resource to be created.</p></li>
<li><p><strong>scopes</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Scopes at which the connection should be applied.</p></li>
<li><p><strong>service_provider_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the service provider that will be associated with this connection. Changing this forces a new resource to be created.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<blockquote>
<div><p>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_connection.html.markdown">https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_connection.html.markdown</a>.</p>
</div></blockquote>
<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.bot_name">
<code class="sig-name descname">bot_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.bot_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the Bot Resource this connection will be associated with. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.client_id">
<code class="sig-name descname">client_id</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.client_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The Client ID that will be used to authenticate with the service provider.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.client_secret">
<code class="sig-name descname">client_secret</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.client_secret" title="Permalink to this definition">¶</a></dt>
<dd><p>The Client Secret that will be used to authenticate with the service provider.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.location">
<code class="sig-name descname">location</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.location" title="Permalink to this definition">¶</a></dt>
<dd><p>The supported Azure location where the resource exists. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.name">
<code class="sig-name descname">name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.name" title="Permalink to this definition">¶</a></dt>
<dd><p>Specifies the name of the Bot Connection. Changing this forces a new resource to be created. Must be globally unique.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.parameters">
<code class="sig-name descname">parameters</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.parameters" title="Permalink to this definition">¶</a></dt>
<dd><p>A map of additional parameters to apply to the connection.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.resource_group_name">
<code class="sig-name descname">resource_group_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.resource_group_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the resource group in which to create the Bot Connection. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.scopes">
<code class="sig-name descname">scopes</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.scopes" title="Permalink to this definition">¶</a></dt>
<dd><p>The Scopes at which the connection should be applied.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.service_provider_name">
<code class="sig-name descname">service_provider_name</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.service_provider_name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the service provider that will be associated with this connection. Changing this forces a new resource to be created.</p>
</dd></dl>

<dl class="attribute">
<dt id="pulumi_azure.bot.Connection.tags">
<code class="sig-name descname">tags</code><em class="property"> = None</em><a class="headerlink" href="#pulumi_azure.bot.Connection.tags" title="Permalink to this definition">¶</a></dt>
<dd><p>A mapping of tags to assign to the resource.</p>
</dd></dl>

<dl class="method">
<dt id="pulumi_azure.bot.Connection.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param">resource_name</em>, <em class="sig-param">id</em>, <em class="sig-param">opts=None</em>, <em class="sig-param">bot_name=None</em>, <em class="sig-param">client_id=None</em>, <em class="sig-param">client_secret=None</em>, <em class="sig-param">location=None</em>, <em class="sig-param">name=None</em>, <em class="sig-param">parameters=None</em>, <em class="sig-param">resource_group_name=None</em>, <em class="sig-param">scopes=None</em>, <em class="sig-param">service_provider_name=None</em>, <em class="sig-param">tags=None</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.Connection.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Connection resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>bot_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the Bot Resource this connection will be associated with. Changing this forces a new resource to be created.</p></li>
<li><p><strong>client_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Client ID that will be used to authenticate with the service provider.</p></li>
<li><p><strong>client_secret</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Client Secret that will be used to authenticate with the service provider.</p></li>
<li><p><strong>location</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The supported Azure location where the resource exists. Changing this forces a new resource to be created.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – Specifies the name of the Bot Connection. Changing this forces a new resource to be created. Must be globally unique.</p></li>
<li><p><strong>parameters</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A map of additional parameters to apply to the connection.</p></li>
<li><p><strong>resource_group_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the resource group in which to create the Bot Connection. Changing this forces a new resource to be created.</p></li>
<li><p><strong>scopes</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Scopes at which the connection should be applied.</p></li>
<li><p><strong>service_provider_name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the service provider that will be associated with this connection. Changing this forces a new resource to be created.</p></li>
<li><p><strong>tags</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A mapping of tags to assign to the resource.</p></li>
</ul>
</dd>
</dl>
<blockquote>
<div><p>This content is derived from <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_connection.html.markdown">https://github.com/terraform-providers/terraform-provider-azurerm/blob/master/website/docs/r/bot_connection.html.markdown</a>.</p>
</div></blockquote>
</dd></dl>

<dl class="method">
<dt id="pulumi_azure.bot.Connection.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param">prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.Connection.translate_output_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of output properties
into a format of their choosing before writing those properties to the resource object.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

<dl class="method">
<dt id="pulumi_azure.bot.Connection.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param">prop</em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_azure.bot.Connection.translate_input_property" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides subclasses of Resource an opportunity to translate names of input properties into
a format of their choosing before sending those properties to the Pulumi engine.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><p><strong>prop</strong> (<em>str</em>) – A property name.</p>
</dd>
<dt class="field-even">Returns</dt>
<dd class="field-even"><p>A potentially transformed property name.</p>
</dd>
<dt class="field-odd">Return type</dt>
<dd class="field-odd"><p>str</p>
</dd>
</dl>
</dd></dl>

</dd></dl>

</div>
