# Day 4 – ConfigMaps & Secrets

## Commands Run
```bash
kubectl apply -f manifests/nginx-configmap.yaml
kubectl apply -f manifests/nginx-secret.yaml
kubectl apply -f manifests/nginx-config-secret-pod.yaml
kubectl get pods
kubectl exec -it nginx-config-secret-pod -- env | grep USERNAME
kubectl exec -it nginx-config-secret-pod -- env | grep PASSWORD
```