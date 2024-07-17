**nginx server**
mkdir nginx_logs nginx_conf

docker-compose up -d

---

**Which Kubernetes command you will use to identify the reason for a pod restart in the project "internal" under namespace "production"**
kubectl get pod -n production --selector=project=internal
kubectl describe pod **POD>** -n production
kubectl logs **POD>** -n production --previous

---

**Java-app keep restarting at random.  From Kubernetes configuration perspective, what are the possible reasons for the pod restarts?**
OOMKilled: If the Java application exceeds the memory limit 1500Mi, Kubernetes might OOMKill the pod, resulting in a restart.
Dependencies: If the application depends on external services, issues with dependencies could cause the pod to restart if these dependencies are not met.
