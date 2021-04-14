# Dev-681
POC Grafana Dashboard reporting NaaS API GW service availability

# Get Prometheus stateful sets, operator deployment and secret
```
kubectl describe -n monitoring statefulset prometheus-monitor-kube-prometheus-st-prometheus > prom.yaml
kubectl describe -n monitoring statefulset alertmanager-monitor-kube-prometheus-st-alertmanager > alert.yaml
kubectl describe -n monitoring deployment monitor-kube-prometheus-st-operator > oper.yaml
kubectl -n monitoring get secret prometheus-monitor-kube-prometheus-st-prometheus -o yaml > secret.yaml
kubectl -n monitoring get configmap prometheus-monitor-kube-prometheus-st-prometheus-rulefiles-0 -o yaml > rules.yaml
```
