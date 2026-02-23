# Day 1 – Cluster Setup & First Pod

## Commands Run
```bash
kubectl cluster-info
kubectl get nodes
kubectl get pods -A
kubectl apply -f manifests/nginx-pod.yaml
kubectl apply -f manifests/nginx-deployment.yaml
kubectl get pods