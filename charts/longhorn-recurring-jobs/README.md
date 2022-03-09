# longhorn-recurring-jobs
Chart for generating Longhorn Recurring Jobs

### How to use

Create a values.yaml for your use case (ex: `your-values.yaml`)
using the original `values.yaml` as a template.

```
helm repo add tyzbit https://tyzbit.github.io/helm-charts
helm install tyzbit/longhorn-recurring-jobs -f your-values.yaml
```
