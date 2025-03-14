# tplink

![Version: 0.3.0](https://img.shields.io/badge/Version-0.3.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

TPLink Exporter

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| devices | list | See values.yaml for an example | Array of devices |
| image.pullPolicy | string | `"Always"` | Image pull policy |
| image.repository | string | `"zibby/tplink-exporter"` | Image repository |
| image.tag | string | `"latest"` | Image tag |
| imagePullSecrets | list | `[]` | Image pull secrets (example: `[{"name": "secretname"}]`) |
| podAnnotations | object | `{}` | Pod annotations |
| replicaCount | int | `1` | Number of replicas |
| resources | object | `{"limits":{"cpu":"100m","memory":"128Mi"},"requests":{"cpu":"100m","memory":"128Mi"}}` | Resource requests and limits |
| service.port | int | `8089` | Service port |
| service.type | string | `"ClusterIP"` | Service type |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
