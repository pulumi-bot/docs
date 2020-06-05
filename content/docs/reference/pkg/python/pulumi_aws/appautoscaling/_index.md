---
title: Module appautoscaling
title_tag: Module appautoscaling | Package pulumi_aws | Python SDK
linktitle: appautoscaling
notitle: true
---

<div class="section" id="appautoscaling">
<h1>appautoscaling<a class="headerlink" href="#appautoscaling" title="Permalink to this headline">¶</a></h1>
<blockquote>
<div><p>This provider is a derived work of the <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws">Terraform Provider</a> distributed under
<a class="reference external" href="https://www.mozilla.org/en-US/MPL/2.0/">MPL 2.0</a>. If you encounter a bug or missing feature, first check the
<a class="reference external" href="https://github.com/pulumi/pulumi-aws/issues">pulumi/pulumi-aws repo</a>; however, if that doesn’t turn up
anything, please consult the source <a class="reference external" href="https://github.com/terraform-providers/terraform-provider-aws/issues">terraform-providers/terraform-provider-aws repo</a>.</p>
</div></blockquote>
<span class="target" id="module-pulumi_aws.appautoscaling"></span><dl class="py class">
<dt id="pulumi_aws.appautoscaling.Policy">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.appautoscaling.</code><code class="sig-name descname">Policy</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">policy_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_dimension</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_namespace</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">step_scaling_policy_configuration</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">target_tracking_scaling_policy_configuration</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an Application AutoScaling Policy resource.</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">dynamodb_table_read_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;dynamodbTableReadTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="s2">&quot;table/tableName&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;dynamodb:table:ReadCapacityUnits&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;dynamodb&quot;</span><span class="p">)</span>
<span class="n">dynamodb_table_read_policy</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Policy</span><span class="p">(</span><span class="s2">&quot;dynamodbTableReadPolicy&quot;</span><span class="p">,</span>
    <span class="n">policy_type</span><span class="o">=</span><span class="s2">&quot;TargetTrackingScaling&quot;</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="n">dynamodb_table_read_target</span><span class="o">.</span><span class="n">resource_id</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="n">dynamodb_table_read_target</span><span class="o">.</span><span class="n">scalable_dimension</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="n">dynamodb_table_read_target</span><span class="o">.</span><span class="n">service_namespace</span><span class="p">,</span>
    <span class="n">target_tracking_scaling_policy_configuration</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;predefinedMetricSpecification&quot;</span><span class="p">:</span> <span class="p">{</span>
            <span class="s2">&quot;predefinedMetricType&quot;</span><span class="p">:</span> <span class="s2">&quot;DynamoDBReadCapacityUtilization&quot;</span><span class="p">,</span>
        <span class="p">},</span>
        <span class="s2">&quot;targetValue&quot;</span><span class="p">:</span> <span class="mi">70</span><span class="p">,</span>
    <span class="p">})</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">ecs_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;ecsTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="s2">&quot;service/clusterName/serviceName&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;ecs:service:DesiredCount&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;ecs&quot;</span><span class="p">)</span>
<span class="n">ecs_policy</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Policy</span><span class="p">(</span><span class="s2">&quot;ecsPolicy&quot;</span><span class="p">,</span>
    <span class="n">policy_type</span><span class="o">=</span><span class="s2">&quot;StepScaling&quot;</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="n">ecs_target</span><span class="o">.</span><span class="n">resource_id</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="n">ecs_target</span><span class="o">.</span><span class="n">scalable_dimension</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="n">ecs_target</span><span class="o">.</span><span class="n">service_namespace</span><span class="p">,</span>
    <span class="n">step_scaling_policy_configuration</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;adjustment_type&quot;</span><span class="p">:</span> <span class="s2">&quot;ChangeInCapacity&quot;</span><span class="p">,</span>
        <span class="s2">&quot;cooldown&quot;</span><span class="p">:</span> <span class="mi">60</span><span class="p">,</span>
        <span class="s2">&quot;metric_aggregation_type&quot;</span><span class="p">:</span> <span class="s2">&quot;Maximum&quot;</span><span class="p">,</span>
        <span class="s2">&quot;stepAdjustment&quot;</span><span class="p">:</span> <span class="p">[{</span>
            <span class="s2">&quot;metricIntervalUpperBound&quot;</span><span class="p">:</span> <span class="mi">0</span><span class="p">,</span>
            <span class="s2">&quot;scaling_adjustment&quot;</span><span class="p">:</span> <span class="o">-</span><span class="mi">1</span><span class="p">,</span>
        <span class="p">}],</span>
    <span class="p">})</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">ecs_service</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">ecs</span><span class="o">.</span><span class="n">Service</span><span class="p">(</span><span class="s2">&quot;ecsService&quot;</span><span class="p">,</span>
    <span class="n">cluster</span><span class="o">=</span><span class="s2">&quot;clusterName&quot;</span><span class="p">,</span>
    <span class="n">desired_count</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span>
    <span class="n">lifecycle</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;ignoreChanges&quot;</span><span class="p">:</span> <span class="p">[</span><span class="s2">&quot;desiredCount&quot;</span><span class="p">],</span>
    <span class="p">},</span>
    <span class="n">task_definition</span><span class="o">=</span><span class="s2">&quot;taskDefinitionFamily:1&quot;</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">replicas_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;replicasTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">15</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="sa">f</span><span class="s2">&quot;cluster:</span><span class="si">{</span><span class="n">aws_rds_cluster</span><span class="p">[</span><span class="s1">&#39;example&#39;</span><span class="p">][</span><span class="s1">&#39;id&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;rds:cluster:ReadReplicaCount&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;rds&quot;</span><span class="p">)</span>
<span class="n">replicas_policy</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Policy</span><span class="p">(</span><span class="s2">&quot;replicasPolicy&quot;</span><span class="p">,</span>
    <span class="n">policy_type</span><span class="o">=</span><span class="s2">&quot;TargetTrackingScaling&quot;</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="n">replicas_target</span><span class="o">.</span><span class="n">resource_id</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="n">replicas_target</span><span class="o">.</span><span class="n">scalable_dimension</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="n">replicas_target</span><span class="o">.</span><span class="n">service_namespace</span><span class="p">,</span>
    <span class="n">target_tracking_scaling_policy_configuration</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;predefinedMetricSpecification&quot;</span><span class="p">:</span> <span class="p">{</span>
            <span class="s2">&quot;predefinedMetricType&quot;</span><span class="p">:</span> <span class="s2">&quot;RDSReaderAverageCPUUtilization&quot;</span><span class="p">,</span>
        <span class="p">},</span>
        <span class="s2">&quot;scaleInCooldown&quot;</span><span class="p">:</span> <span class="mi">300</span><span class="p">,</span>
        <span class="s2">&quot;scaleOutCooldown&quot;</span><span class="p">:</span> <span class="mi">300</span><span class="p">,</span>
        <span class="s2">&quot;targetValue&quot;</span><span class="p">:</span> <span class="mi">75</span><span class="p">,</span>
    <span class="p">})</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the policy.</p></li>
<li><p><strong>policy_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The policy type. Valid values are <code class="docutils literal notranslate"><span class="pre">StepScaling</span></code> and <code class="docutils literal notranslate"><span class="pre">TargetTrackingScaling</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">StepScaling</span></code>. Certain services only support only one policy type. For more information see the <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html">Target Tracking Scaling Policies</a> and <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-step-scaling-policies.html">Step Scaling Policies</a> documentation.</p></li>
<li><p><strong>resource_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The resource type and unique identifier string for the resource associated with the scaling policy. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ResourceId</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p></li>
<li><p><strong>scalable_dimension</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The scalable dimension of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ScalableDimension</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>service_namespace</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The AWS service namespace of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ServiceNamespace</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>step_scaling_policy_configuration</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – Step scaling policy configuration, requires <code class="docutils literal notranslate"><span class="pre">policy_type</span> <span class="pre">=</span> <span class="pre">&quot;StepScaling&quot;</span></code> (default). See supported fields below.</p></li>
<li><p><strong>target_tracking_scaling_policy_configuration</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A target tracking policy, requires <code class="docutils literal notranslate"><span class="pre">policy_type</span> <span class="pre">=</span> <span class="pre">&quot;TargetTrackingScaling&quot;</span></code>. See supported fields below.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>step_scaling_policy_configuration</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">adjustment_type</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies whether the adjustment is an absolute number or a percentage of the current capacity. Valid values are <code class="docutils literal notranslate"><span class="pre">ChangeInCapacity</span></code>, <code class="docutils literal notranslate"><span class="pre">ExactCapacity</span></code>, and <code class="docutils literal notranslate"><span class="pre">PercentChangeInCapacity</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">cooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The amount of time, in seconds, after a scaling activity completes and before the next scaling activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">metric_aggregation_type</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The aggregation type for the policy’s metrics. Valid values are “Minimum”, “Maximum”, and “Average”. Without a value, AWS will treat the aggregation type as “Average”.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">min_adjustment_magnitude</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The minimum number to adjust your scalable dimension as a result of a scaling activity. If the adjustment type is PercentChangeInCapacity, the scaling policy changes the scalable dimension of the scalable target by this amount.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">step_adjustments</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - A set of adjustments that manage scaling. These have the following structure:</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">metricIntervalLowerBound</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>)</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">metricIntervalUpperBound</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>)</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaling_adjustment</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>)</p></li>
</ul>
</li>
</ul>
<p>The <strong>target_tracking_scaling_policy_configuration</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">customizedMetricSpecification</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[dict]</span></code>) - A custom CloudWatch metric. Documentation can be found  at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CustomizedMetricSpecification.html">AWS Customized Metric Specification</a>. See supported fields below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">dimensions</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Configuration block(s) with the dimensions of the metric if the metric was published with dimensions. Detailed below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the policy.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Value of the dimension.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">metric_name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the metric.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">namespace</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The namespace of the metric.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">statistic</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The statistic of the metric. Valid values: <code class="docutils literal notranslate"><span class="pre">Average</span></code>, <code class="docutils literal notranslate"><span class="pre">Minimum</span></code>, <code class="docutils literal notranslate"><span class="pre">Maximum</span></code>, <code class="docutils literal notranslate"><span class="pre">SampleCount</span></code>, and <code class="docutils literal notranslate"><span class="pre">Sum</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">unit</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The unit of the metric.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">disableScaleIn</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[bool]</span></code>) - Indicates whether scale in by the target tracking policy is disabled. If the value is true, scale in is disabled and the target tracking policy won’t remove capacity from the scalable resource. Otherwise, scale in is enabled and the target tracking policy can remove capacity from the scalable resource. The default value is <code class="docutils literal notranslate"><span class="pre">false</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">predefinedMetricSpecification</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[dict]</span></code>) - A predefined metric. See supported fields below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">predefinedMetricType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The metric type.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceLabel</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Reserved for future use.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaleInCooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The amount of time, in seconds, after a scale in activity completes before another scale in activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaleOutCooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The amount of time, in seconds, after a scale out activity completes before another scale out activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">targetValue</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The target value for the metric.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.arn">
<code class="sig-name descname">arn</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The ARN assigned by AWS to the scaling policy.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the policy.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.policy_type">
<code class="sig-name descname">policy_type</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.policy_type" title="Permalink to this definition">¶</a></dt>
<dd><p>The policy type. Valid values are <code class="docutils literal notranslate"><span class="pre">StepScaling</span></code> and <code class="docutils literal notranslate"><span class="pre">TargetTrackingScaling</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">StepScaling</span></code>. Certain services only support only one policy type. For more information see the <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html">Target Tracking Scaling Policies</a> and <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-step-scaling-policies.html">Step Scaling Policies</a> documentation.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.resource_id">
<code class="sig-name descname">resource_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.resource_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The resource type and unique identifier string for the resource associated with the scaling policy. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ResourceId</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.scalable_dimension">
<code class="sig-name descname">scalable_dimension</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.scalable_dimension" title="Permalink to this definition">¶</a></dt>
<dd><p>The scalable dimension of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ScalableDimension</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.service_namespace">
<code class="sig-name descname">service_namespace</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.service_namespace" title="Permalink to this definition">¶</a></dt>
<dd><p>The AWS service namespace of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ServiceNamespace</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.step_scaling_policy_configuration">
<code class="sig-name descname">step_scaling_policy_configuration</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.step_scaling_policy_configuration" title="Permalink to this definition">¶</a></dt>
<dd><p>Step scaling policy configuration, requires <code class="docutils literal notranslate"><span class="pre">policy_type</span> <span class="pre">=</span> <span class="pre">&quot;StepScaling&quot;</span></code> (default). See supported fields below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">adjustment_type</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Specifies whether the adjustment is an absolute number or a percentage of the current capacity. Valid values are <code class="docutils literal notranslate"><span class="pre">ChangeInCapacity</span></code>, <code class="docutils literal notranslate"><span class="pre">ExactCapacity</span></code>, and <code class="docutils literal notranslate"><span class="pre">PercentChangeInCapacity</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">cooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The amount of time, in seconds, after a scaling activity completes and before the next scaling activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">metric_aggregation_type</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The aggregation type for the policy’s metrics. Valid values are “Minimum”, “Maximum”, and “Average”. Without a value, AWS will treat the aggregation type as “Average”.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">min_adjustment_magnitude</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The minimum number to adjust your scalable dimension as a result of a scaling activity. If the adjustment type is PercentChangeInCapacity, the scaling policy changes the scalable dimension of the scalable target by this amount.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">step_adjustments</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - A set of adjustments that manage scaling. These have the following structure:</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">metricIntervalLowerBound</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>)</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">metricIntervalUpperBound</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>)</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaling_adjustment</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>)</p></li>
</ul>
</li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Policy.target_tracking_scaling_policy_configuration">
<code class="sig-name descname">target_tracking_scaling_policy_configuration</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.target_tracking_scaling_policy_configuration" title="Permalink to this definition">¶</a></dt>
<dd><p>A target tracking policy, requires <code class="docutils literal notranslate"><span class="pre">policy_type</span> <span class="pre">=</span> <span class="pre">&quot;TargetTrackingScaling&quot;</span></code>. See supported fields below.</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">customizedMetricSpecification</span></code> (<code class="docutils literal notranslate"><span class="pre">dict</span></code>) - A custom CloudWatch metric. Documentation can be found  at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CustomizedMetricSpecification.html">AWS Customized Metric Specification</a>. See supported fields below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">dimensions</span></code> (<code class="docutils literal notranslate"><span class="pre">list</span></code>) - Configuration block(s) with the dimensions of the metric if the metric was published with dimensions. Detailed below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The name of the policy.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Value of the dimension.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">metric_name</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The name of the metric.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">namespace</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The namespace of the metric.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">statistic</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The statistic of the metric. Valid values: <code class="docutils literal notranslate"><span class="pre">Average</span></code>, <code class="docutils literal notranslate"><span class="pre">Minimum</span></code>, <code class="docutils literal notranslate"><span class="pre">Maximum</span></code>, <code class="docutils literal notranslate"><span class="pre">SampleCount</span></code>, and <code class="docutils literal notranslate"><span class="pre">Sum</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">unit</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The unit of the metric.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">disableScaleIn</span></code> (<code class="docutils literal notranslate"><span class="pre">bool</span></code>) - Indicates whether scale in by the target tracking policy is disabled. If the value is true, scale in is disabled and the target tracking policy won’t remove capacity from the scalable resource. Otherwise, scale in is enabled and the target tracking policy can remove capacity from the scalable resource. The default value is <code class="docutils literal notranslate"><span class="pre">false</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">predefinedMetricSpecification</span></code> (<code class="docutils literal notranslate"><span class="pre">dict</span></code>) - A predefined metric. See supported fields below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">predefinedMetricType</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - The metric type.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceLabel</span></code> (<code class="docutils literal notranslate"><span class="pre">str</span></code>) - Reserved for future use.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaleInCooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The amount of time, in seconds, after a scale in activity completes before another scale in activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaleOutCooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The amount of time, in seconds, after a scale out activity completes before another scale out activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">targetValue</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The target value for the metric.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.Policy.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">policy_type</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_dimension</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_namespace</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">step_scaling_policy_configuration</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">target_tracking_scaling_policy_configuration</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Policy resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ARN assigned by AWS to the scaling policy.</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the policy.</p></li>
<li><p><strong>policy_type</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The policy type. Valid values are <code class="docutils literal notranslate"><span class="pre">StepScaling</span></code> and <code class="docutils literal notranslate"><span class="pre">TargetTrackingScaling</span></code>. Defaults to <code class="docutils literal notranslate"><span class="pre">StepScaling</span></code>. Certain services only support only one policy type. For more information see the <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-target-tracking.html">Target Tracking Scaling Policies</a> and <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/application-auto-scaling-step-scaling-policies.html">Step Scaling Policies</a> documentation.</p>
</p></li>
<li><p><strong>resource_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The resource type and unique identifier string for the resource associated with the scaling policy. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ResourceId</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>scalable_dimension</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The scalable dimension of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ScalableDimension</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>service_namespace</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The AWS service namespace of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ServiceNamespace</span></code> parameter at: <a class="reference external" href="http://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>step_scaling_policy_configuration</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – Step scaling policy configuration, requires <code class="docutils literal notranslate"><span class="pre">policy_type</span> <span class="pre">=</span> <span class="pre">&quot;StepScaling&quot;</span></code> (default). See supported fields below.</p></li>
<li><p><strong>target_tracking_scaling_policy_configuration</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – A target tracking policy, requires <code class="docutils literal notranslate"><span class="pre">policy_type</span> <span class="pre">=</span> <span class="pre">&quot;TargetTrackingScaling&quot;</span></code>. See supported fields below.</p></li>
</ul>
</dd>
</dl>
<p>The <strong>step_scaling_policy_configuration</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">adjustment_type</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Specifies whether the adjustment is an absolute number or a percentage of the current capacity. Valid values are <code class="docutils literal notranslate"><span class="pre">ChangeInCapacity</span></code>, <code class="docutils literal notranslate"><span class="pre">ExactCapacity</span></code>, and <code class="docutils literal notranslate"><span class="pre">PercentChangeInCapacity</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">cooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The amount of time, in seconds, after a scaling activity completes and before the next scaling activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">metric_aggregation_type</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The aggregation type for the policy’s metrics. Valid values are “Minimum”, “Maximum”, and “Average”. Without a value, AWS will treat the aggregation type as “Average”.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">min_adjustment_magnitude</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The minimum number to adjust your scalable dimension as a result of a scaling activity. If the adjustment type is PercentChangeInCapacity, the scaling policy changes the scalable dimension of the scalable target by this amount.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">step_adjustments</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - A set of adjustments that manage scaling. These have the following structure:</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">metricIntervalLowerBound</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>)</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">metricIntervalUpperBound</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>)</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaling_adjustment</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>)</p></li>
</ul>
</li>
</ul>
<p>The <strong>target_tracking_scaling_policy_configuration</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">customizedMetricSpecification</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[dict]</span></code>) - A custom CloudWatch metric. Documentation can be found  at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_CustomizedMetricSpecification.html">AWS Customized Metric Specification</a>. See supported fields below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">dimensions</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[list]</span></code>) - Configuration block(s) with the dimensions of the metric if the metric was published with dimensions. Detailed below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the policy.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">value</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Value of the dimension.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">metric_name</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The name of the metric.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">namespace</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The namespace of the metric.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">statistic</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The statistic of the metric. Valid values: <code class="docutils literal notranslate"><span class="pre">Average</span></code>, <code class="docutils literal notranslate"><span class="pre">Minimum</span></code>, <code class="docutils literal notranslate"><span class="pre">Maximum</span></code>, <code class="docutils literal notranslate"><span class="pre">SampleCount</span></code>, and <code class="docutils literal notranslate"><span class="pre">Sum</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">unit</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The unit of the metric.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">disableScaleIn</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[bool]</span></code>) - Indicates whether scale in by the target tracking policy is disabled. If the value is true, scale in is disabled and the target tracking policy won’t remove capacity from the scalable resource. Otherwise, scale in is enabled and the target tracking policy can remove capacity from the scalable resource. The default value is <code class="docutils literal notranslate"><span class="pre">false</span></code>.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">predefinedMetricSpecification</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[dict]</span></code>) - A predefined metric. See supported fields below.</p>
<ul>
<li><p><code class="docutils literal notranslate"><span class="pre">predefinedMetricType</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - The metric type.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">resourceLabel</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[str]</span></code>) - Reserved for future use.</p></li>
</ul>
</li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaleInCooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The amount of time, in seconds, after a scale in activity completes before another scale in activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">scaleOutCooldown</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The amount of time, in seconds, after a scale out activity completes before another scale out activity can start.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">targetValue</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The target value for the metric.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.Policy.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.translate_output_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.Policy.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Policy.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py class">
<dt id="pulumi_aws.appautoscaling.ScheduledAction">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.appautoscaling.</code><code class="sig-name descname">ScheduledAction</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">end_time</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_dimension</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_target_action</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">schedule</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_namespace</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">start_time</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an Application AutoScaling ScheduledAction resource.</p>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">dynamodb_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;dynamodbTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="s2">&quot;table/tableName&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;dynamodb:table:ReadCapacityUnits&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;dynamodb&quot;</span><span class="p">)</span>
<span class="n">dynamodb_scheduled_action</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">ScheduledAction</span><span class="p">(</span><span class="s2">&quot;dynamodbScheduledAction&quot;</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="n">dynamodb_target</span><span class="o">.</span><span class="n">resource_id</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="n">dynamodb_target</span><span class="o">.</span><span class="n">scalable_dimension</span><span class="p">,</span>
    <span class="n">scalable_target_action</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;max_capacity&quot;</span><span class="p">:</span> <span class="mi">200</span><span class="p">,</span>
        <span class="s2">&quot;min_capacity&quot;</span><span class="p">:</span> <span class="mi">1</span><span class="p">,</span>
    <span class="p">},</span>
    <span class="n">schedule</span><span class="o">=</span><span class="s2">&quot;at(2006-01-02T15:04:05)&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="n">dynamodb_target</span><span class="o">.</span><span class="n">service_namespace</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">ecs_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;ecsTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="s2">&quot;service/clusterName/serviceName&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;ecs:service:DesiredCount&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;ecs&quot;</span><span class="p">)</span>
<span class="n">ecs_scheduled_action</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">ScheduledAction</span><span class="p">(</span><span class="s2">&quot;ecsScheduledAction&quot;</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="n">ecs_target</span><span class="o">.</span><span class="n">resource_id</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="n">ecs_target</span><span class="o">.</span><span class="n">scalable_dimension</span><span class="p">,</span>
    <span class="n">scalable_target_action</span><span class="o">=</span><span class="p">{</span>
        <span class="s2">&quot;max_capacity&quot;</span><span class="p">:</span> <span class="mi">10</span><span class="p">,</span>
        <span class="s2">&quot;min_capacity&quot;</span><span class="p">:</span> <span class="mi">1</span><span class="p">,</span>
    <span class="p">},</span>
    <span class="n">schedule</span><span class="o">=</span><span class="s2">&quot;at(2006-01-02T15:04:05)&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="n">ecs_target</span><span class="o">.</span><span class="n">service_namespace</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>end_time</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The date and time for the scheduled action to end. Specify the following format: 2006-01-02T15:04:05Z</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the scheduled action.</p></li>
<li><p><strong>resource_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The identifier of the resource associated with the scheduled action. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ResourceId">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>scalable_dimension</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The scalable dimension. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ScalableDimension">AWS Application Auto Scaling API Reference</a> Example: ecs:service:DesiredCount</p>
</p></li>
<li><p><strong>scalable_target_action</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – The new minimum and maximum capacity. You can set both values or just one. See below</p></li>
<li><p><strong>schedule</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The schedule for this action. The following formats are supported: At expressions - at(yyyy-mm-ddThh:mm:ss), Rate expressions - rate(valueunit), Cron expressions - cron(fields). In UTC. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-Schedule">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>service_namespace</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The namespace of the AWS service. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ServiceNamespace">AWS Application Auto Scaling API Reference</a> Example: ecs</p>
</p></li>
<li><p><strong>start_time</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The date and time for the scheduled action to start. Specify the following format: 2006-01-02T15:04:05Z</p></li>
</ul>
</dd>
</dl>
<p>The <strong>scalable_target_action</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">max_capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The maximum capacity.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">min_capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The minimum capacity.</p></li>
</ul>
<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.arn">
<code class="sig-name descname">arn</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The Amazon Resource Name (ARN) of the scheduled action.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.end_time">
<code class="sig-name descname">end_time</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.end_time" title="Permalink to this definition">¶</a></dt>
<dd><p>The date and time for the scheduled action to end. Specify the following format: 2006-01-02T15:04:05Z</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.name">
<code class="sig-name descname">name</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.name" title="Permalink to this definition">¶</a></dt>
<dd><p>The name of the scheduled action.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.resource_id">
<code class="sig-name descname">resource_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.resource_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The identifier of the resource associated with the scheduled action. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ResourceId">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.scalable_dimension">
<code class="sig-name descname">scalable_dimension</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.scalable_dimension" title="Permalink to this definition">¶</a></dt>
<dd><p>The scalable dimension. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ScalableDimension">AWS Application Auto Scaling API Reference</a> Example: ecs:service:DesiredCount</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.scalable_target_action">
<code class="sig-name descname">scalable_target_action</code><em class="property">: pulumi.Output[dict]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.scalable_target_action" title="Permalink to this definition">¶</a></dt>
<dd><p>The new minimum and maximum capacity. You can set both values or just one. See below</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">max_capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The maximum capacity.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">min_capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">float</span></code>) - The minimum capacity.</p></li>
</ul>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.schedule">
<code class="sig-name descname">schedule</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.schedule" title="Permalink to this definition">¶</a></dt>
<dd><p>The schedule for this action. The following formats are supported: At expressions - at(yyyy-mm-ddThh:mm:ss), Rate expressions - rate(valueunit), Cron expressions - cron(fields). In UTC. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-Schedule">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.service_namespace">
<code class="sig-name descname">service_namespace</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.service_namespace" title="Permalink to this definition">¶</a></dt>
<dd><p>The namespace of the AWS service. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ServiceNamespace">AWS Application Auto Scaling API Reference</a> Example: ecs</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.start_time">
<code class="sig-name descname">start_time</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.start_time" title="Permalink to this definition">¶</a></dt>
<dd><p>The date and time for the scheduled action to start. Specify the following format: 2006-01-02T15:04:05Z</p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">end_time</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">name</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_dimension</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_target_action</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">schedule</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_namespace</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">start_time</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing ScheduledAction resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The Amazon Resource Name (ARN) of the scheduled action.</p></li>
<li><p><strong>end_time</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The date and time for the scheduled action to end. Specify the following format: 2006-01-02T15:04:05Z</p></li>
<li><p><strong>name</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The name of the scheduled action.</p></li>
<li><p><strong>resource_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The identifier of the resource associated with the scheduled action. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ResourceId">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>scalable_dimension</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The scalable dimension. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ScalableDimension">AWS Application Auto Scaling API Reference</a> Example: ecs:service:DesiredCount</p>
</p></li>
<li><p><strong>scalable_target_action</strong> (<em>pulumi.Input</em><em>[</em><em>dict</em><em>]</em>) – The new minimum and maximum capacity. You can set both values or just one. See below</p></li>
<li><p><strong>schedule</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The schedule for this action. The following formats are supported: At expressions - at(yyyy-mm-ddThh:mm:ss), Rate expressions - rate(valueunit), Cron expressions - cron(fields). In UTC. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-Schedule">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>service_namespace</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The namespace of the AWS service. Documentation can be found in the parameter at: <a class="reference external" href="https://docs.aws.amazon.com/ApplicationAutoScaling/latest/APIReference/API_PutScheduledAction.html#ApplicationAutoScaling-PutScheduledAction-request-ServiceNamespace">AWS Application Auto Scaling API Reference</a> Example: ecs</p>
</p></li>
<li><p><strong>start_time</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The date and time for the scheduled action to start. Specify the following format: 2006-01-02T15:04:05Z</p></li>
</ul>
</dd>
</dl>
<p>The <strong>scalable_target_action</strong> object supports the following:</p>
<ul class="simple">
<li><p><code class="docutils literal notranslate"><span class="pre">max_capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The maximum capacity.</p></li>
<li><p><code class="docutils literal notranslate"><span class="pre">min_capacity</span></code> (<code class="docutils literal notranslate"><span class="pre">pulumi.Input[float]</span></code>) - The minimum capacity.</p></li>
</ul>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.translate_output_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.ScheduledAction.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.ScheduledAction.translate_input_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py class">
<dt id="pulumi_aws.appautoscaling.Target">
<em class="property">class </em><code class="sig-prename descclassname">pulumi_aws.appautoscaling.</code><code class="sig-name descname">Target</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">max_capacity</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">min_capacity</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">role_arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_dimension</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_namespace</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__props__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__name__</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">__opts__</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Target" title="Permalink to this definition">¶</a></dt>
<dd><p>Provides an Application AutoScaling ScalableTarget resource. To manage policies which get attached to the target, see the <code class="docutils literal notranslate"><span class="pre">appautoscaling.Policy</span></code> resource.</p>
<blockquote>
<div><p><strong>NOTE:</strong> The <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/security_iam_service-with-iam.html#security_iam_service-with-iam-roles">Application Auto Scaling service automatically attempts to manage IAM Service-Linked Roles</a> when registering certain service namespaces for the first time. To manually manage this role, see the <code class="docutils literal notranslate"><span class="pre">iam.ServiceLinkedRole</span></code> resource.</p>
</div></blockquote>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">dynamodb_table_read_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;dynamodbTableReadTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="sa">f</span><span class="s2">&quot;table/</span><span class="si">{</span><span class="n">aws_dynamodb_table</span><span class="p">[</span><span class="s1">&#39;example&#39;</span><span class="p">][</span><span class="s1">&#39;name&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;dynamodb:table:ReadCapacityUnits&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;dynamodb&quot;</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">dynamodb_index_read_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;dynamodbIndexReadTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">100</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">5</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="sa">f</span><span class="s2">&quot;table/</span><span class="si">{</span><span class="n">aws_dynamodb_table</span><span class="p">[</span><span class="s1">&#39;example&#39;</span><span class="p">][</span><span class="s1">&#39;name&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">/index/</span><span class="si">{</span><span class="n">var</span><span class="p">[</span><span class="s1">&#39;index_name&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;dynamodb:index:ReadCapacityUnits&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;dynamodb&quot;</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">ecs_target</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;ecsTarget&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">4</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="sa">f</span><span class="s2">&quot;service/</span><span class="si">{</span><span class="n">aws_ecs_cluster</span><span class="p">[</span><span class="s1">&#39;example&#39;</span><span class="p">][</span><span class="s1">&#39;name&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">/</span><span class="si">{</span><span class="n">aws_ecs_service</span><span class="p">[</span><span class="s1">&#39;example&#39;</span><span class="p">][</span><span class="s1">&#39;name&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;ecs:service:DesiredCount&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;ecs&quot;</span><span class="p">)</span>
</pre></div>
</div>
<div class="highlight-python notranslate"><div class="highlight"><pre><span></span><span class="kn">import</span> <span class="nn">pulumi</span>
<span class="kn">import</span> <span class="nn">pulumi_aws</span> <span class="k">as</span> <span class="nn">aws</span>

<span class="n">replicas</span> <span class="o">=</span> <span class="n">aws</span><span class="o">.</span><span class="n">appautoscaling</span><span class="o">.</span><span class="n">Target</span><span class="p">(</span><span class="s2">&quot;replicas&quot;</span><span class="p">,</span>
    <span class="n">max_capacity</span><span class="o">=</span><span class="mi">15</span><span class="p">,</span>
    <span class="n">min_capacity</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span>
    <span class="n">resource_id</span><span class="o">=</span><span class="sa">f</span><span class="s2">&quot;cluster:</span><span class="si">{</span><span class="n">aws_rds_cluster</span><span class="p">[</span><span class="s1">&#39;example&#39;</span><span class="p">][</span><span class="s1">&#39;id&#39;</span><span class="p">]</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">,</span>
    <span class="n">scalable_dimension</span><span class="o">=</span><span class="s2">&quot;rds:cluster:ReadReplicaCount&quot;</span><span class="p">,</span>
    <span class="n">service_namespace</span><span class="o">=</span><span class="s2">&quot;rds&quot;</span><span class="p">)</span>
</pre></div>
</div>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The name of the resource.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>max_capacity</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max capacity of the scalable target.</p></li>
<li><p><strong>min_capacity</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The min capacity of the scalable target.</p></li>
<li><p><strong>resource_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The resource type and unique identifier string for the resource associated with the scaling policy. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ResourceId</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>role_arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – The ARN of the IAM role that allows Application AutoScaling to modify your scalable target on your behalf. This defaults to an IAM Service-Linked Role for most services and custom IAM Roles are ignored by the API for those namespaces. See the <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/security_iam_service-with-iam.html#security_iam_service-with-iam-roles">AWS Application Auto Scaling documentation</a> for more information about how this service interacts with IAM.</p></li>
<li><p><strong>scalable_dimension</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The scalable dimension of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ScalableDimension</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>service_namespace</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The AWS service namespace of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ServiceNamespace</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
</ul>
</dd>
</dl>
<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Target.max_capacity">
<code class="sig-name descname">max_capacity</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.max_capacity" title="Permalink to this definition">¶</a></dt>
<dd><p>The max capacity of the scalable target.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Target.min_capacity">
<code class="sig-name descname">min_capacity</code><em class="property">: pulumi.Output[float]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.min_capacity" title="Permalink to this definition">¶</a></dt>
<dd><p>The min capacity of the scalable target.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Target.resource_id">
<code class="sig-name descname">resource_id</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.resource_id" title="Permalink to this definition">¶</a></dt>
<dd><p>The resource type and unique identifier string for the resource associated with the scaling policy. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ResourceId</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Target.role_arn">
<code class="sig-name descname">role_arn</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.role_arn" title="Permalink to this definition">¶</a></dt>
<dd><p>The ARN of the IAM role that allows Application AutoScaling to modify your scalable target on your behalf. This defaults to an IAM Service-Linked Role for most services and custom IAM Roles are ignored by the API for those namespaces. See the <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/security_iam_service-with-iam.html#security_iam_service-with-iam-roles">AWS Application Auto Scaling documentation</a> for more information about how this service interacts with IAM.</p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Target.scalable_dimension">
<code class="sig-name descname">scalable_dimension</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.scalable_dimension" title="Permalink to this definition">¶</a></dt>
<dd><p>The scalable dimension of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ScalableDimension</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py attribute">
<dt id="pulumi_aws.appautoscaling.Target.service_namespace">
<code class="sig-name descname">service_namespace</code><em class="property">: pulumi.Output[str]</em><em class="property"> = None</em><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.service_namespace" title="Permalink to this definition">¶</a></dt>
<dd><p>The AWS service namespace of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ServiceNamespace</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.Target.get">
<em class="property">static </em><code class="sig-name descname">get</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">resource_name</span></em>, <em class="sig-param"><span class="n">id</span></em>, <em class="sig-param"><span class="n">opts</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">max_capacity</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">min_capacity</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">resource_id</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">role_arn</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">scalable_dimension</span><span class="o">=</span><span class="default_value">None</span></em>, <em class="sig-param"><span class="n">service_namespace</span><span class="o">=</span><span class="default_value">None</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.get" title="Permalink to this definition">¶</a></dt>
<dd><p>Get an existing Target resource’s state with the given name, id, and optional extra
properties used to qualify the lookup.</p>
<dl class="field-list simple">
<dt class="field-odd">Parameters</dt>
<dd class="field-odd"><ul class="simple">
<li><p><strong>resource_name</strong> (<em>str</em>) – The unique name of the resulting resource.</p></li>
<li><p><strong>id</strong> (<em>str</em>) – The unique provider ID of the resource to lookup.</p></li>
<li><p><strong>opts</strong> (<a class="reference internal" href="../../pulumi/#pulumi.ResourceOptions" title="pulumi.ResourceOptions"><em>pulumi.ResourceOptions</em></a>) – Options for the resource.</p></li>
<li><p><strong>max_capacity</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The max capacity of the scalable target.</p></li>
<li><p><strong>min_capacity</strong> (<em>pulumi.Input</em><em>[</em><em>float</em><em>]</em>) – The min capacity of the scalable target.</p></li>
<li><p><strong>resource_id</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The resource type and unique identifier string for the resource associated with the scaling policy. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ResourceId</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>role_arn</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The ARN of the IAM role that allows Application AutoScaling to modify your scalable target on your behalf. This defaults to an IAM Service-Linked Role for most services and custom IAM Roles are ignored by the API for those namespaces. See the <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/userguide/security_iam_service-with-iam.html#security_iam_service-with-iam-roles">AWS Application Auto Scaling documentation</a> for more information about how this service interacts with IAM.</p>
</p></li>
<li><p><strong>scalable_dimension</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The scalable dimension of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ScalableDimension</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
<li><p><strong>service_namespace</strong> (<em>pulumi.Input</em><em>[</em><em>str</em><em>]</em>) – <p>The AWS service namespace of the scalable target. Documentation can be found in the <code class="docutils literal notranslate"><span class="pre">ServiceNamespace</span></code> parameter at: <a class="reference external" href="https://docs.aws.amazon.com/autoscaling/application/APIReference/API_RegisterScalableTarget.html#API_RegisterScalableTarget_RequestParameters">AWS Application Auto Scaling API Reference</a></p>
</p></li>
</ul>
</dd>
</dl>
</dd></dl>

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.Target.translate_output_property">
<code class="sig-name descname">translate_output_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.translate_output_property" title="Permalink to this definition">¶</a></dt>
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

<dl class="py method">
<dt id="pulumi_aws.appautoscaling.Target.translate_input_property">
<code class="sig-name descname">translate_input_property</code><span class="sig-paren">(</span><em class="sig-param"><span class="n">prop</span></em><span class="sig-paren">)</span><a class="headerlink" href="#pulumi_aws.appautoscaling.Target.translate_input_property" title="Permalink to this definition">¶</a></dt>
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
