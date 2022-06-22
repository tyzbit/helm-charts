# grav

Modern, Crazy Fast, Ridiculously Easy and Amazingly Powerful Flat-File CMS powered by PHP, Markdown, Twig, and Symfony

![Version: 0.7.0](https://img.shields.io/badge/Version-0.7.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Installing the Chart

To install the chart with the release name `example`:

```console
helm repo add tyzbit https://tyzbit.github.io/helm-charts
helm install example tyzbit/grav -f your-values.yaml
```

## Multisite
Enable multisite:
```yaml
grav:
  config:
    GRAV_MULTISITE: subdirectory
```

You can also specify `subdomain`.

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| deploymentAnnotations | object | `{}` | Annotations to add to the deployment (grav) |
| filebrowser.affinity | object | `{}` | Filebrowser pod affinity |
| filebrowser.args | list | `["-p","8000","-d","/db/database.db"]` | Arguments for the filebrowser container |
| filebrowser.enabled | bool | `false` | Enable filebrowser, an app that lets you edit the contents of the data volume via web GUI. Default credentials `admin/admin` |
| filebrowser.image.pullPolicy | string | `"IfNotPresent"` | Kubernetes imagePullPolicy for the filebrowser container |
| filebrowser.image.repository | string | `"filebrowser/filebrowser"` | Docker image repo for the filebrowser image |
| filebrowser.image.tag | string | `"v2"` | Docker image tag to deploy for filebrowser |
| filebrowser.nodeSelector | object | `{}` | Specify a specific node to run filebrowser on |
| filebrowser.service.port | int | `8000` | Service port for the filebrowser frontend service |
| filebrowser.subdomain | string | `"files"` | What subdomain filebrowser should be available at |
| filebrowser.tolerations | list | `[]` | Filebrowser pod tolerations |
| fullnameOverride | string | `""` | Override the full name |
| grav.affinity | object | `{}` | Grav pod affinity |
| grav.config | object | `{}` | Specify environment variables (in key: "value" notation) |
| grav.customPHPini | string | `"upload_max_filesize = 256M\npost_max_size = 256M"` | Custom PHP parameters |
| grav.image.pullPolicy | string | `"IfNotPresent"` | Kubernetes imagePullPolicy for the grav container |
| grav.image.repository | string | `"tyzbit/grav"` | Docker image repo for the grav image |
| grav.image.tag | string | `"latest"` | Docker image tag to deploy for grav, `admin` installs grav with the admin plugin |
| grav.nodeSelector | object | `{}` | Specify a specific node to run grav on |
| grav.probes.enabled | bool | `true` | Enable startup, readiness and liveness probes for grav |
| grav.probes.liveness.initialDelaySeconds | int | `10` | Initial delay for the liveness probe |
| grav.probes.liveness.timeoutSeconds | int | `2` | Probe timeout |
| grav.probes.readiness.initialDelaySeconds | int | `10` | Initial delay for the readiness probe |
| grav.probes.readiness.timeoutSeconds | int | `2` | Probe timeout |
| grav.probes.startup.failureThreshold | int | `30` | Failure threshold |
| grav.probes.startup.initialDelaySeconds | int | `10` | Initial delay for the startup probe |
| grav.probes.startup.periodSeconds | int | `2` | How many seconds between probes |
| grav.probes.startup.timeoutSeconds | int | `2` | Probe timeout |
| grav.resources | object | `{}` | Resource limits for the grav container |
| grav.service.port | int | `80` | Service port for the grav frontend service |
| grav.tolerations | list | `[]` | Grav pod tolerations |
| imagePullSecrets | list | `[]` | List imagePullSecrets to use when pulling Docker containers |
| ingress.annotations | object | `{}` | Annotations for the ingress |
| ingress.className | string | `""` | Class name for the ingress |
| ingress.enabled | bool | `true` | Enable the ingress |
| ingress.hosts[0].host | string | `"chart-example.local"` | Hostname for the grav site |
| ingress.hosts[0].paths[0].path | string | `"/"` | Path to the grav site off of the host |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` | Path type for matching |
| ingress.tls | list | `[]` | Kubernetes TLS secret ( example: `[ secretName: chart-example-tls, hosts: [ chart-example.local ] ]`) |
| nameOverride | string | `""` | Override the release name |
| persistence.accessModes | list | `["ReadWriteMany"]` | Persistent Volume access modes |
| persistence.enabled | bool | `false` | Enable persistence of data (you probably want this) |
| persistence.existingClaimName | string | `""` | Use an existing PersistentVolumeClaim |
| persistence.size | string | `"10Gi"` | Size to provision for the Persistent Volume |
| persistence.storageClass | string | `""` | Kubernetes StorageClass for the PersistentVolume |
| podAnnotations | object | `{}` | Annotations for the grav container |
| podSecurityContext | object | `{}` | Security context for the grav container |
| replicaCount | int | `1` | How many deployment pods for Grav |
| securityContext | object | `{}` | Security context for all containers in the pod |
| service.type | string | `"ClusterIP"` | Service type for the grav frontend service |
| statefulSetAnnotations | object | `{}` | Annotations to add to the statefulset (filebrowser) |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.8.1](https://github.com/norwoodj/helm-docs/releases/v1.8.1)
