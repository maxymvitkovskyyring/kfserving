<p>Packages:</p>
<ul>
<li>
<a href="#serving.kubeflow.org%2fv1alpha2">serving.kubeflow.org/v1alpha2</a>
</li>
</ul>
<h2 id="serving.kubeflow.org/v1alpha2">serving.kubeflow.org/v1alpha2</h2>
<p>
<p>Package v1alpha2 contains API Schema definitions for the serving v1alpha2 API group</p>
</p>
Resource Types:
<ul><li>
<a href="#serving.kubeflow.org/v1alpha2.InferenceService">InferenceService</a>
</li></ul>
<h3 id="serving.kubeflow.org/v1alpha2.InferenceService">InferenceService
</h3>
<p>
<p>InferenceService is the Schema for the services API</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>apiVersion</code></br>
string</td>
<td>
<code>
serving.kubeflow.org/v1alpha2
</code>
</td>
</tr>
<tr>
<td>
<code>kind</code></br>
string
</td>
<td><code>InferenceService</code></td>
</tr>
<tr>
<td>
<code>metadata</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#objectmeta-v1-meta">
Kubernetes meta/v1.ObjectMeta
</a>
</em>
</td>
<td>
Refer to the Kubernetes API documentation for the fields of the
<code>metadata</code> field.
</td>
</tr>
<tr>
<td>
<code>spec</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.InferenceServiceSpec">
InferenceServiceSpec
</a>
</em>
</td>
<td>
<br/>
<br/>
<table>
<tr>
<td>
<code>default</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">
EndpointSpec
</a>
</em>
</td>
<td>
<p>Default defines default InferenceService endpoints</p>
</td>
</tr>
<tr>
<td>
<code>canary</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">
EndpointSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Canary defines an alternate endpoints to route a percentage of traffic.</p>
</td>
</tr>
<tr>
<td>
<code>canaryTrafficPercent</code></br>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>CanaryTrafficPercent defines the percentage of traffic going to canary InferenceService endpoints</p>
</td>
</tr>
</table>
</td>
</tr>
<tr>
<td>
<code>status</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.InferenceServiceStatus">
InferenceServiceStatus
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.AlibiExplainerSpec">AlibiExplainerSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.ExplainerSpec">ExplainerSpec</a>)
</p>
<p>
<p>AlibiExplainerSpec defines the arguments for configuring an Alibi Explanation Server</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>type</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.AlibiExplainerType">
AlibiExplainerType
</a>
</em>
</td>
<td>
<p>The type of Alibi explainer</p>
</td>
</tr>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of a trained explanation model</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Defaults to latest Alibi Version</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
<tr>
<td>
<code>config</code></br>
<em>
map[string]string
</em>
</td>
<td>
<p>Inline custom parameter settings for explainer</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.AlibiExplainerType">AlibiExplainerType
(<code>string</code> alias)</p></h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.AlibiExplainerSpec">AlibiExplainerSpec</a>)
</p>
<p>
</p>
<h3 id="serving.kubeflow.org/v1alpha2.CustomSpec">CustomSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.ExplainerSpec">ExplainerSpec</a>, 
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>, 
<a href="#serving.kubeflow.org/v1alpha2.TransformerSpec">TransformerSpec</a>)
</p>
<p>
<p>CustomSpec provides a hook for arbitrary container configuration.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>container</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#container-v1-core">
Kubernetes core/v1.Container
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.DeploymentSpec">DeploymentSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.ExplainerSpec">ExplainerSpec</a>, 
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>, 
<a href="#serving.kubeflow.org/v1alpha2.TransformerSpec">TransformerSpec</a>)
</p>
<p>
<p>DeploymentSpec defines the configuration for a given InferenceService service component</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>serviceAccountName</code></br>
<em>
string
</em>
</td>
<td>
<em>(Optional)</em>
<p>ServiceAccountName is the name of the ServiceAccount to use to run the service</p>
</td>
</tr>
<tr>
<td>
<code>minReplicas</code></br>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>Minimum number of replicas, pods won&rsquo;t scale down to 0 in case of no traffic</p>
</td>
</tr>
<tr>
<td>
<code>maxReplicas</code></br>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>This is the up bound for autoscaler to scale to</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.EndpointSpec">EndpointSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.InferenceServiceSpec">InferenceServiceSpec</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>predictor</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">
PredictorSpec
</a>
</em>
</td>
<td>
<p>Predictor defines the model serving spec</p>
</td>
</tr>
<tr>
<td>
<code>explainer</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.ExplainerSpec">
ExplainerSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Explainer defines the model explanation service spec,
explainer service calls to predictor or transformer if it is specified.</p>
</td>
</tr>
<tr>
<td>
<code>transformer</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.TransformerSpec">
TransformerSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Transformer defines the pre/post processing before and after the predictor call,
transformer service calls to predictor service.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.EndpointStatusMap">EndpointStatusMap
(<code>map[invalid type]*github.com/yuzisun/kfserving/pkg/apis/serving/v1alpha2.StatusConfigurationSpec</code> alias)</p></h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.InferenceServiceStatus">InferenceServiceStatus</a>)
</p>
<p>
<p>EndpointStatusMap defines the observed state of InferenceService endpoints</p>
</p>
<h3 id="serving.kubeflow.org/v1alpha2.Explainer">Explainer
</h3>
<p>
</p>
<h3 id="serving.kubeflow.org/v1alpha2.ExplainerConfig">ExplainerConfig
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.ExplainersConfig">ExplainersConfig</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>image</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>defaultImageVersion</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>allowedImageVersions</code></br>
<em>
[]string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.ExplainerSpec">ExplainerSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">EndpointSpec</a>)
</p>
<p>
<p>ExplainerSpec defines the arguments for a model explanation server,
The following fields follow a &ldquo;1-of&rdquo; semantic. Users must specify exactly one spec.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>alibi</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.AlibiExplainerSpec">
AlibiExplainerSpec
</a>
</em>
</td>
<td>
<p>Spec for alibi explainer</p>
</td>
</tr>
<tr>
<td>
<code>custom</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.CustomSpec">
CustomSpec
</a>
</em>
</td>
<td>
<p>Spec for a custom explainer</p>
</td>
</tr>
<tr>
<td>
<code>DeploymentSpec</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.DeploymentSpec">
DeploymentSpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>DeploymentSpec</code> are embedded into this type.)
</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.ExplainersConfig">ExplainersConfig
</h3>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>alibi</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.ExplainerConfig">
ExplainerConfig
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.InferenceServiceSpec">InferenceServiceSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.InferenceService">InferenceService</a>)
</p>
<p>
<p>InferenceServiceSpec defines the desired state of InferenceService</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>default</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">
EndpointSpec
</a>
</em>
</td>
<td>
<p>Default defines default InferenceService endpoints</p>
</td>
</tr>
<tr>
<td>
<code>canary</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">
EndpointSpec
</a>
</em>
</td>
<td>
<em>(Optional)</em>
<p>Canary defines an alternate endpoints to route a percentage of traffic.</p>
</td>
</tr>
<tr>
<td>
<code>canaryTrafficPercent</code></br>
<em>
int
</em>
</td>
<td>
<em>(Optional)</em>
<p>CanaryTrafficPercent defines the percentage of traffic going to canary InferenceService endpoints</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.InferenceServiceStatus">InferenceServiceStatus
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.InferenceService">InferenceService</a>)
</p>
<p>
<p>InferenceServiceStatus defines the observed state of InferenceService</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>Status</code></br>
<em>
knative.dev/pkg/apis/duck/v1beta1.Status
</em>
</td>
<td>
<p>
(Members of <code>Status</code> are embedded into this type.)
</p>
</td>
</tr>
<tr>
<td>
<code>url</code></br>
<em>
string
</em>
</td>
<td>
<p>URL of the InferenceService</p>
</td>
</tr>
<tr>
<td>
<code>traffic</code></br>
<em>
int
</em>
</td>
<td>
<p>Traffic percentage that goes to default services</p>
</td>
</tr>
<tr>
<td>
<code>canaryTraffic</code></br>
<em>
int
</em>
</td>
<td>
<p>Traffic percentage that goes to canary services</p>
</td>
</tr>
<tr>
<td>
<code>default</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointStatusMap">
EndpointStatusMap
</a>
</em>
</td>
<td>
<p>Statuses for the default endpoints of the InferenceService</p>
</td>
</tr>
<tr>
<td>
<code>canary</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointStatusMap">
EndpointStatusMap
</a>
</em>
</td>
<td>
<p>Statuses for the canary endpoints of the InferenceService</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.ONNXSpec">ONNXSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>)
</p>
<p>
<p>ONNXSpec defines arguments for configuring ONNX model serving.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of the trained model</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Allowed runtime versions are [v0.5.0, latest] and defaults to the version specified in kfservice config map</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.Predictor">Predictor
</h3>
<p>
</p>
<h3 id="serving.kubeflow.org/v1alpha2.PredictorConfig">PredictorConfig
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorsConfig">PredictorsConfig</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>image</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>defaultImageVersion</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>defaultGpuImageVersion</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>allowedImageVersions</code></br>
<em>
[]string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">EndpointSpec</a>)
</p>
<p>
<p>PredictorSpec defines the configuration for a predictor,
The following fields follow a &ldquo;1-of&rdquo; semantic. Users must specify exactly one spec.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>custom</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.CustomSpec">
CustomSpec
</a>
</em>
</td>
<td>
<p>Spec for a custom predictor</p>
</td>
</tr>
<tr>
<td>
<code>tensorflow</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.TensorflowSpec">
TensorflowSpec
</a>
</em>
</td>
<td>
<p>Spec for Tensorflow Serving (<a href="https://github.com/tensorflow/serving">https://github.com/tensorflow/serving</a>)</p>
</td>
</tr>
<tr>
<td>
<code>tensorrt</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.TensorRTSpec">
TensorRTSpec
</a>
</em>
</td>
<td>
<p>Spec for TensorRT Inference Server (<a href="https://github.com/NVIDIA/tensorrt-inference-server">https://github.com/NVIDIA/tensorrt-inference-server</a>)</p>
</td>
</tr>
<tr>
<td>
<code>xgboost</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.XGBoostSpec">
XGBoostSpec
</a>
</em>
</td>
<td>
<p>Spec for XGBoost predictor</p>
</td>
</tr>
<tr>
<td>
<code>sklearn</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.SKLearnSpec">
SKLearnSpec
</a>
</em>
</td>
<td>
<p>Spec for SKLearn predictor</p>
</td>
</tr>
<tr>
<td>
<code>onnx</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.ONNXSpec">
ONNXSpec
</a>
</em>
</td>
<td>
<p>Spec for ONNX runtime (<a href="https://github.com/microsoft/onnxruntime">https://github.com/microsoft/onnxruntime</a>)</p>
</td>
</tr>
<tr>
<td>
<code>pytorch</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PyTorchSpec">
PyTorchSpec
</a>
</em>
</td>
<td>
<p>Spec for PyTorch predictor</p>
</td>
</tr>
<tr>
<td>
<code>DeploymentSpec</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.DeploymentSpec">
DeploymentSpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>DeploymentSpec</code> are embedded into this type.)
</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.PredictorsConfig">PredictorsConfig
</h3>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>tensorflow</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorConfig">
PredictorConfig
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>tensorrt</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorConfig">
PredictorConfig
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>xgboost</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorConfig">
PredictorConfig
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>sklearn</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorConfig">
PredictorConfig
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>pytorch</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorConfig">
PredictorConfig
</a>
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>onnx</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorConfig">
PredictorConfig
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.PyTorchSpec">PyTorchSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>)
</p>
<p>
<p>PyTorchSpec defines arguments for configuring PyTorch model serving.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of the trained model</p>
</td>
</tr>
<tr>
<td>
<code>modelClassName</code></br>
<em>
string
</em>
</td>
<td>
<p>Defaults PyTorch model class name to &lsquo;PyTorchModel&rsquo;</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Allowed runtime versions are [0.2.0, latest] and defaults to the version specified in kfservice config map</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.SKLearnSpec">SKLearnSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>)
</p>
<p>
<p>SKLearnSpec defines arguments for configuring SKLearn model serving.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of the trained model</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Allowed runtime versions are [0.2.0, latest] and defaults to the version specified in kfservice config map</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.StatusConfigurationSpec">StatusConfigurationSpec
</h3>
<p>
<p>StatusConfigurationSpec describes the state of the configuration receiving traffic.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>name</code></br>
<em>
string
</em>
</td>
<td>
<p>Latest revision name that is in ready state</p>
</td>
</tr>
<tr>
<td>
<code>host</code></br>
<em>
string
</em>
</td>
<td>
<p>Host name of the service</p>
</td>
</tr>
<tr>
<td>
<code>replicas</code></br>
<em>
int
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.TensorRTSpec">TensorRTSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>)
</p>
<p>
<p>TensorRTSpec defines arguments for configuring TensorRT model serving.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of the trained model</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Allowed runtime versions are [19.05-py3] and defaults to the version specified in kfservice config map</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.TensorflowSpec">TensorflowSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>)
</p>
<p>
<p>TensorflowSpec defines arguments for configuring Tensorflow model serving.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of the trained model</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Allowed runtime versions are [1.11.0, 1.12.0, 1.13.0, 1.14.0, latest] or [1.11.0-gpu, 1.12.0-gpu, 1.13.0-gpu, 1.14.0-gpu, latest-gpu]
if gpu resource is specified and defaults to the version specified in kfservice config map.</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.Transformer">Transformer
</h3>
<p>
<p>Transformer interface is implemented by all Transformers</p>
</p>
<h3 id="serving.kubeflow.org/v1alpha2.TransformerConfig">TransformerConfig
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.TransformersConfig">TransformersConfig</a>)
</p>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>image</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>defaultImageVersion</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>allowedImageVersions</code></br>
<em>
[]string
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.TransformerSpec">TransformerSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.EndpointSpec">EndpointSpec</a>)
</p>
<p>
<p>TransformerSpec defines transformer service for pre/post processing</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>custom</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.CustomSpec">
CustomSpec
</a>
</em>
</td>
<td>
<p>Spec for a custom transformer</p>
</td>
</tr>
<tr>
<td>
<code>DeploymentSpec</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.DeploymentSpec">
DeploymentSpec
</a>
</em>
</td>
<td>
<p>
(Members of <code>DeploymentSpec</code> are embedded into this type.)
</p>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.TransformersConfig">TransformersConfig
</h3>
<p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>feast</code></br>
<em>
<a href="#serving.kubeflow.org/v1alpha2.TransformerConfig">
TransformerConfig
</a>
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.VirtualServiceStatus">VirtualServiceStatus
</h3>
<p>
<p>VirtualServiceStatus captures the status of the virtual service</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>URL</code></br>
<em>
string
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>CanaryWeight</code></br>
<em>
int
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>DefaultWeight</code></br>
<em>
int
</em>
</td>
<td>
</td>
</tr>
<tr>
<td>
<code>Status</code></br>
<em>
knative.dev/pkg/apis/duck/v1beta1.Status
</em>
</td>
<td>
</td>
</tr>
</tbody>
</table>
<h3 id="serving.kubeflow.org/v1alpha2.XGBoostSpec">XGBoostSpec
</h3>
<p>
(<em>Appears on:</em>
<a href="#serving.kubeflow.org/v1alpha2.PredictorSpec">PredictorSpec</a>)
</p>
<p>
<p>XGBoostSpec defines arguments for configuring XGBoost model serving.</p>
</p>
<table>
<thead>
<tr>
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>
<code>storageUri</code></br>
<em>
string
</em>
</td>
<td>
<p>The location of the trained model</p>
</td>
</tr>
<tr>
<td>
<code>runtimeVersion</code></br>
<em>
string
</em>
</td>
<td>
<p>Allowed runtime versions are [0.2.0, latest] and defaults to the version specified in kfservice config map</p>
</td>
</tr>
<tr>
<td>
<code>resources</code></br>
<em>
<a href="https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.13/#resourcerequirements-v1-core">
Kubernetes core/v1.ResourceRequirements
</a>
</em>
</td>
<td>
<p>Defaults to requests and limits of 1CPU, 2Gb MEM.</p>
</td>
</tr>
</tbody>
</table>
<hr/>
<p><em>
Generated with <code>gen-crd-api-reference-docs</code>
on git commit <code>52e137b</code>.
</em></p>
