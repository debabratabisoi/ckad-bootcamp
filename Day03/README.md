# Day 3 – Probes (Liveness, Readiness, Startup)

## Commands Run
```bash
kubectl apply -f manifests/nginx-probes.yaml
kubectl get pods
kubectl describe pod <pod-name>
kubectl delete pod <pod-name>   # to observe restart behavior
```