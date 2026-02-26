# Day 6 – StatefulSets & Headless Services

## Commands Run
```bash
kubectl apply -f manifests/mysql-headless-service.yaml
kubectl apply -f manifests/mysql-statefulset.yaml
kubectl get pods
kubectl get svc
kubectl describe statefulset mysql
```
## Real-World Case Study
Imagine a banking application running on Kubernetes:
The app requires a MySQL database cluster with multiple replicas.
Each replica must have a stable identity (mysql-0, mysql-1, mysql-2) so data replication can be configured.
A StatefulSet ensures pods are created in order and retain their identity across restarts.
A Headless Service provides DNS records for each pod (mysql-0.mysql, mysql-1.mysql, etc.), allowing the database cluster to communicate internally.
This setup is critical for stateful workloads like databases, message queues, or distributed storage systems.

# Notes
StatefulSets = ordered, stable pods with persistent storage.
Headless Service = DNS records for each pod, no load balancing.
Together, they enable reliable database clusters inside Kubernetes.