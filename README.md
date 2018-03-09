## notes
Tested on a clean k8s v1.9.0 minikube install.

## simple demo
###### add scrape-metrics-ports-only annotation to all kube-dns pods
    kubectl --namespace=kube-system patch deployment kube-dns -p "$(cat k8s-kube-dns-patch.yaml)"

###### create the monitoring namespace:
    kubectl apply -f k8s-monitoring-namespace.yaml

###### deploy a prometheus instance
    kubectl apply -f k8s-prometheus

###### view the prometheus web ui in your default browser
    minikube service --namespace monitoring  prometheus

## todo
- demo installation of kube-state-metrics (kubernetes/kube-state-metrics)
- demo installation of grafana
  - build or find working dashboards and make sure they're version controlled