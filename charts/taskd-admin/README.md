# my0n/taskd-admin

The official helm chart for [taskd-admin](https://github.com/my0n/taskd-admin).

**This chart is not a part of the taskwarrior organization and any issues with the chart should be raised [here](https://github.com/my0n/helm-charts/issues/new).**

## Example usage

Install the helm chart:

```sh
helm repo add my0n https://my0n.github.io/helm-charts
helm repo update
helm install taskd-admin my0n/taskd-admin -f values.yaml
```

Sample values.yaml given below; see [values.yaml](values.yaml) for more details.

```yaml
# values.yaml
# TODO
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | Defines affinity constraint rules. Read more about `affinity` [here](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity). |
| fullnameOverride | string | `""` | Override for full name of generated resources. |
| image.pullPolicy | string | `"IfNotPresent"` | Image pull policy. |
| image.repository | string | `"ghcr.io/my0n/taskd-admin"` | Image repository. |
| image.tag | string | `""` | Image tag. |
| imagePullSecrets | list | `[]` | Secrets for pulling an image. |
| ingress.annotations | object | `{}` | Provide additional ingress annotations if needed. |
| ingress.enabled | bool | `false` | Enables or disables the ingress. |
| ingress.host | string | `"chart-example.local"` | Host address. |
| ingress.path | string | `"/"` | Path. |
| ingress.pathType | string | `"ImplementationSpecific"` | Ignored if not kubeVersion >= 1.18-0 |
| ingress.tls | list | `[]` | Configure TLS for the ingress. |
| nameOverride | string | `""` | Override for name of generated resources. |
| nodeSelector | object | `{}` | Defines node selection constraints. Read more about `nodeSelector` [here](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#nodeselector). |
| persistence.existingClaim | string | `""` | Use an existing Persistent Volume Claim. |
| podAnnotations | object | `{}` | Annotations for the server pod. |
| podSecurityContext | object | `{}` | Pod security context. |
| resources | object | `{}` | Set the resource limits/requests for the pod. |
| securityContext | object | `{}` | Security context. |
| service.port | int | `53589` | The port for the service. |
| service.type | string | `"ClusterIP"` | The type of service. |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account. |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created. |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and `serviceAccount.create` is true, a name is generated using the fullname template. |
| tolerations | list | `[]` | Specify taint tolerations. Read more about `tolerations` [here](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/). |