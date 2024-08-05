# gitlab-arm64-pangarabbit

A Helm Chart for Gitlab ARM64

![Version: 0.1.14](https://img.shields.io/badge/Version-0.1.14-informational?style=flat-square)
![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)
![AppVersion: 17.0](https://img.shields.io/badge/AppVersion-17.0-informational?style=flat-square)

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Sacha Wharton | <sacha@pangarabbit.com> | <https://github.com/sachajw> |

## Installing the Chart

To install the chart with the release name `gitlab-arm64`:

```console
$ helm repo add gitlab-arm64 https://sachajw.github.io/gitlab-helm-chart-pangarabbit
$ helm repo update
$ helm install gitlab-arm64 gitlab-arm64/gitlab-arm64-pangarabbit
```

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://chart.onechart.dev | onechart | 0.6.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| container | object | `{}` |  |
| containerPort | int | `80` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"zengxs/gitlab"` |  |
| image.tag | string | `"17.0"` |  |
| ingress.annotations."cert-manager.io/cluster-issuer" | string | `"letsencrypt-staging"` |  |
| ingress.host | string | `"chart-example.local"` |  |
| ingress.ingressClassName | string | `"traefik"` |  |
| ingress.nginxBasicAuth.password | string | `"secret"` |  |
| ingress.nginxBasicAuth.user | string | `"admin"` |  |
| ingress.tlsEnabled | bool | `true` |  |
| livenessProbe.enabled | bool | `false` |  |
| livenessProbe.path | string | `"/"` |  |
| livenessProbe.settings.failureThreshold | int | `3` |  |
| livenessProbe.settings.initialDelaySeconds | int | `0` |  |
| livenessProbe.settings.periodSeconds | int | `10` |  |
| livenessProbe.settings.successThreshold | int | `1` |  |
| livenessProbe.settings.timeoutSeconds | int | `3` |  |
| monitor.enabled | bool | `false` |  |
| nameOverride | string | `""` |  |
| nodePortEnabled | bool | `false` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podDisruptionBudgetEnabled | bool | `true` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.fsGroup | int | `999` |  |
| podSpec | object | `{}` |  |
| probe.enabled | bool | `false` |  |
| probe.path | string | `"/"` |  |
| probe.settings.failureThreshold | int | `3` |  |
| probe.settings.initialDelaySeconds | int | `0` |  |
| probe.settings.periodSeconds | int | `10` |  |
| probe.settings.successThreshold | int | `1` |  |
| probe.settings.timeoutSeconds | int | `3` |  |
| replicas | int | `1` |  |
| resources.limits.cpu | string | `"200m"` |  |
| resources.limits.memory | string | `"200Mi"` |  |
| resources.requests.cpu | string | `"200m"` |  |
| resources.requests.memory | string | `"200Mi"` |  |
| secretEnabled | bool | `false` |  |
| securityContext | object | `{}` |  |
| shell | string | `"/bin/sh"` |  |
| spreadAcrossNodes | bool | `false` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
