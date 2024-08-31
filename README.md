### Prerequisites
1. Kubernetes Cluster
2. Grafana Cloud Account
3. Kubectl
4. Helm

### Backend Installation
Install required alert rules and recording rules to this Grafana instance.

### Enter cluster information
Cluster name: iquant-k8s
Namespace: monitoring

### Generate Grafana Access Policy Token
Token Name: iquant-k8s-token

### Deploy using Helm
Run the values.yaml file using the command: 

```
helm repo add grafana https://grafana.github.io/helm-charts \
&& helm repo update \
&& helm upgrade --install --atomic --timeout 300s grafana-k8s-monitoring grafana/k8s-monitoring \
--namespace "monitoring" --create-namespace --values values.yaml
```

### Explore your data
On the Grafana Cloud, go to homepage to see visualized metrics

