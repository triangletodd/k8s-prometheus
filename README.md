Tested on a clean k8s v1.9.0 minikube install.

# demo:

`kubectl --namespace=kube-system patch deployment kube-dns -p "$(cat k8s-kube-dns-patch.yaml)"`

`kubectl apply -f k8s-monitoring-namespace.yaml`

`kubectl apply -f k8s-prometheus`

`minikube service --namespace monitoring  prometheus`

# todo:

- demo installation of https://github.com/kubernetes/kube-state-metrics/
- demo isntallation of grafana
  - include working grafana dashboards