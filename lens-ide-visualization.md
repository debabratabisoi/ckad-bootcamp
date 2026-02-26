🔍 Lens IDE Navigation Guide
1. kubectl get pods
Lens view: Go to Workloads → Pods.
You’ll see all pods listed, their status (Running, Pending, CrashLoopBackOff), and logs/events.

Example: After applying nginx-pv-pod.yaml, you’ll see nginx-pv-pod here.

2. kubectl get deployments
Lens view: Workloads → Deployments.
Shows replica count, desired vs. available pods, and rollout status.

Example: nginx-deployment scaling from 2 → 5 replicas will be visible here.

3. kubectl get svc
Lens view: Network → Services.
Displays service type (ClusterIP, NodePort, LoadBalancer), ports, and endpoints.

Example: nginx-service will appear here with port 80 mapped internally.

4. kubectl get pv / kubectl get pvc
Lens view: Storage → Persistent Volumes / Persistent Volume Claims.
Shows capacity, access modes, and binding status.

Example: nginx-pv bound to nginx-pvc will show as Bound.

5. kubectl describe statefulset mysql
Lens view: Workloads → StatefulSets.
Displays ordered pods (mysql-0, mysql-1, mysql-2) with stable identities.

Example: You’ll see each pod listed with its own persistent volume claim.

6. Probes (Day 3)
Lens view: Workloads → Pods → Pod Details → Containers.
Under each container, you’ll see Liveness/Readiness/Startup probes configured.

Example: nginx-probes deployment will show probe definitions here.

7. Logs & Events
Lens view: Select any Pod → Logs tab.
Useful for debugging probe failures, PVC binding issues, or container crashes.