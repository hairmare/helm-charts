# caasperli

![Version: 0.9.0](https://img.shields.io/badge/Version-0.9.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.2](https://img.shields.io/badge/AppVersion-v0.2-informational?style=flat-square)

Deploy Caasperli to a Kubernetes Cluster

**Homepage:** <https://github.com/adfinis-sygroup/potz-holzoepfel-und-zipfelchape>

## Maintainers
This chart is maintained by [Adfinis](https://adfinis.com/?pk_campaign=github&pk_kwd=helm-charts).

## Source Code

* <https://github.com/adfinis-sygroup/potz-holzoepfel-und-zipfelchape>
* <https://github.com/adfinis-sygroup/helm-charts/tree/master/charts/caasperli>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | mongodb | ~9.0.1 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| deploymentAnnotations | object | `{}` | Annotations to add to Deployment. |
| fullnameOverride | string | `""` |  |
| grafana.enabled | bool | `false` | Enable Grafana Dashboards |
| grafana.extraLabels | object | `{}` | Labels to add to all Grafana integration resources |
| image.pullPolicy | string | `"Always"` | When to pull the container image |
| image.repository | string | `"adfinissygroup/potz-holzoepfel-und-zipfelchape"` | Container image to deploy |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` | Annotations to add to the ingress resource |
| ingress.enabled | bool | `false` | Enable ingress |
| ingress.hosts | list | `[{"host":"chart-example.local","paths":[]}]` | List of hosts to expose via ingress |
| ingress.tls | list | `[]` | TLS configuration for ingress |
| mongodb.enabled | bool | `false` | Enable MongoDB "stateful" deploy |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` | Annotations to add to Pod. |
| podSecurityContext | object | `{}` | [PodSecurityContext](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.18/#podsecuritycontext-v1-core) |
| prometheus.enabled | bool | `false` | Enable Prometheus integration |
| prometheus.extraLabels | object | `{}` | Labels to add to all Prometheus integration resources |
| prometheus.podMonitor.enabled | bool | `true` | Enable creation of a PodMonitor CRD |
| prometheus.podMonitor.interval | string | `"30s"` | Interval at which metrics should be scraped |
| prometheus.podMonitor.metricRelabelings | list | `[]` | MetricRelabelConfigs to apply to samples before ingestion |
| prometheus.podMonitor.relabelings | list | `[]` | RelabelConfigs to apply to samples before scraping |
| prometheus.serviceMonitor.enabled | bool | `false` | Enable creation of a ServiceMonitor CRD |
| prometheus.serviceMonitor.interval | string | `"30s"` | Interval at which metrics should be scraped |
| prometheus.serviceMonitor.metricRelabelings | list | `[]` | MetricRelabelConfigs to apply to samples before ingestion |
| prometheus.serviceMonitor.relabelings | list | `[]` | RelabelConfigs to apply to samples before scraping |
| replicaCount | int | `1` | How many caasperlis to deploy |
| resources | object | `{}` |  |
| securityContext | object | `{}` | [SecurityContext](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.18/#securitycontext-v1-core) |
| service.port | int | `80` | Port the service will expose |
| service.type | string | `"ClusterIP"` | Type of the service to create |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` |  |

## About this chart

Adfinis fights for a software world that is more open, where the quality is
better and where software must be accessible to everyone. This chart
is part of the action behind this commitment. Feel free to
[contact](https://adfinis.com/kontakt/?pk_campaign=github&pk_kwd=helm-charts)
us if you have any questions.

## License

This Helm chart is free software: you can redistribute it and/or modify it under the terms
of the GNU Affero General Public License as published by the Free Software Foundation,
version 3 of the License.
