# longhorn-recurring-jobs

Longhorn Recurring Jobs Generator

![Version: 2.1.0](https://img.shields.io/badge/Version-2.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

## Installing the Chart

To install the chart with the release name `example`:

```console
helm repo add tyzbit https://tyzbit.github.io/helm-charts
helm install example tyzbit/longhorn-recurring-jobs -f your-values.yaml
```

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| allowVolumeExpansion | bool | `true` | Default StorageClass properties. |
| createStorageClasses | bool | `false` | Optionally create storageclasses for each group. This is disabled by default because the Helm release will fail if an upgrade is run and it tries to remove an in-use StorageClass. |
| defaultConcurrency | int | `4` | Default job concurrency |
| hourStep | int | `2` |  |
| minuteStep | int | `5` | How separated should the minutes and hours be on the generated cron expressions. Example: if minuteStep: 5, then the cron expression will be like "0/10 * * * *", "5/10 * * * *" |
| namespaceOverride | string | `""` |  |
| parameters | object | See values.yaml for an example | Longhorn-specific parameters. |
| reclaimPolicy | string | `"Retain"` |  |
| spreadCronStartTimes | bool | `true` | Whether or not to spread the jobs so that the start times are "randomized" (actually deterministic). If this is false, minutes and hours in generated cron expressions will be 0 Examples if true: "15/30 * * * *" "5/15 4 * * *" Examples if false: "0 * * * *" "0 0/2 * * *" |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.8.1](https://github.com/norwoodj/helm-docs/releases/v1.8.1)
