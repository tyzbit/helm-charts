# inspector

Inspector uses his gadgets to inspect whatever you want!

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Installing the Chart

To install the chart with the release name `example`:

```console
helm repo add tyzbit https://tyzbit.github.io/helm-charts
helm install example tyzbit/inspector -f your-values.yaml
```

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| additionalMounts | object | `{}` | Additional mounts (`[ name: name, mountPath: /path ]`) |
| additionalVolumes | object | `{}` | Additional volumes (`[ name: name, persistentVolumeClaim: { claimName: /path } ]`) |
| image.pullPolicy | string | `"Always"` | Image pull policy |
| image.repository | string | `"tyzbit/inspector"` | Image repository for Inspector |
| image.tag | string | `"latest"` | Image tag |
| imagePullSecrets | string | `nil` | Docker image pull secrets |
| podAnnotations | string | `nil` | Annotations for the pod |
| resources | object | `{}` | Resources for the container |
| storageClassName | string | `"default"` | StorageClass name for the inspector configs |
| tolerations | object | `{}` | Tolerations |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
