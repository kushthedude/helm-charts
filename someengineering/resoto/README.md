# resoto

![Version: 0.3.10](https://img.shields.io/badge/Version-0.3.10-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.4.1](https://img.shields.io/badge/AppVersion-2.4.1-informational?style=flat-square)

A Helm chart for Kubernetes

**Homepage:** <https://resoto.com>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| kushthedude |  |  |
| aquamatthias | <eng@some.engineering> |  |

## Source Code

* <https://github.com/someengineering/resoto>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common(common) | 2.0.2 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| imagePullPolicy | string | `"IfNotPresent"` | The image pull policy |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resotocore.extraArgs | list | `[]` | Use this section to define extra arguments |
| resotocore.extraEnv | list | `[]` | Use this section to pass extra environment variables |
| resotocore.graphdb | object | `{"database":"resoto","passwordSecret":{"key":"password","name":"arango-user"},"server":"http://single-server:8529","username":"resoto"}` | This defines the access to the graph database |
| resotocore.graphdb.database | string | `"resoto"` | The name of the database to use |
| resotocore.graphdb.passwordSecret | object | `{"key":"password","name":"arango-user"}` | The secret to get the password from |
| resotocore.graphdb.passwordSecret.key | string | `"password"` | The secret key to get the password from |
| resotocore.graphdb.passwordSecret.name | string | `"arango-user"` | The secret name to get the password from |
| resotocore.graphdb.server | string | `"http://single-server:8529"` | The complete url of the graph database |
| resotocore.graphdb.username | string | `"resoto"` | The name of the user to connect |
| resotocore.image.repository | string | `"somecr.io/someengineering/resotocore"` | Image repository |
| resotocore.image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| resotocore.ingress.annotations | object | `{}` |  |
| resotocore.ingress.className | string | `""` |  |
| resotocore.ingress.enabled | bool | `false` |  |
| resotocore.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| resotocore.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| resotocore.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| resotocore.ingress.tls | list | `[]` |  |
| resotocore.overrides | list | `["resotocore.runtime.start_collect_on_subscriber_connect=true","resotocore.api.ui_path=/usr/local/resoto/ui/"]` | Use this section to override configuration values |
| resotocore.overrides[0] | string | `"resotocore.runtime.start_collect_on_subscriber_connect=true"` | start a collect cycle automatically when the first collector is connected |
| resotocore.overrides[1] | string | `"resotocore.api.ui_path=/usr/local/resoto/ui/"` | this is location of the UI in the docker container |
| resotocore.service.port | int | `8900` |  |
| resotocore.service.type | string | `"ClusterIP"` |  |
| resotometrics.extraArgs | list | `[]` | Use this section to define extra arguments |
| resotometrics.extraEnv | list | `[]` | Use this section to pass extra environment variables |
| resotometrics.image.repository | string | `"somecr.io/someengineering/resotometrics"` | Image repository |
| resotometrics.image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| resotometrics.overrides | list | `[]` | Use this section to override configuration values |
| resotometrics.serviceMonitor | object | `{"enabled":false,"interval":"30s","scrapeTimeout":"25s"}` | Prometheus serviceMonitor configuration |
| resotometrics.serviceMonitor.enabled | bool | `false` | Whether a Prometheus serviceMonitor should be created |
| resotometrics.serviceMonitor.interval | string | `"30s"` | Metrics scrape interval |
| resotometrics.serviceMonitor.scrapeTimeout | string | `"25s"` | Metrics scrape timeout |
| resotoworker.extraArgs | list | `[]` | Use this section to define extra arguments |
| resotoworker.extraEnv | list | `[]` | Use this section to pass extra environment variables |
| resotoworker.image.repository | string | `"somecr.io/someengineering/resotoworker"` | Image repository |
| resotoworker.image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| resotoworker.overrides | list | `[]` | Use this section to override configuration values |
| resotoworker.volumeMounts | list | `[]` | Use this section to define volume mounts for the worker |
| resotoworker.volumes | list | `[]` | Use this section to define volumes of the worker |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | If not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
