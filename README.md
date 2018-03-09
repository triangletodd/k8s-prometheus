On a clean minikube installation:

`kubectl --namespace=kube-system patch deployment kube-dns -p "$(cat k8s-kube-dns-patch.yaml)"`

`kubectl apply -f k8s-monitoring-namespace.yaml`

`kubectl apply -f k8s-prometheus`

`minikube service --namespace monitoring  prometheus`
