# Day 5 – Persistent Volumes & Claims

## Commands Run
```bash
kubectl apply -f manifests/pv.yaml
kubectl apply -f manifests/pvc.yaml
kubectl get pv
kubectl get pvc
kubectl apply -f manifests/nginx-pv-pod.yaml
kubectl get pods
kubectl exec -it nginx-pv-pod -- /bin/bash

## Real-World Case Study
Imagine an e-commerce application running on Kubernetes:

The frontend (nginx) serves product pages.
Product images and static content must persist even if the Pod restarts.
Using a Persistent Volume (PV) ensures data is stored on the node’s disk.
A Persistent Volume Claim (PVC) allows the Pod to request storage without worrying about the underlying infrastructure.
In production, instead of hostPath, cloud providers use managed storage (AWS EBS, Azure Disk, GCP Persistent Disk).

This way, even if the nginx Pod crashes or is rescheduled, the product images remain intact and available.

# Notes
PV defines actual storage resource.
PVC is a request for storage by a Pod.
Pod mounts PVC to persist data across restarts.