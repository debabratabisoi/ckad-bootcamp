# Daily Sanity Check

Run these commands after reboot to verify cluster health:

```bash
docker ps
minikube start --driver=docker
kubectl cluster-info
kubectl get nodes
kubectl get pods -A
