**Kubectl Basic Commands**

**1. Cluster Info**

```bash
kubectl version                         # Show client and server version
kubectl cluster-info                   # Display cluster info
kubectl config view                    # View kubeconfig settings
kubectl get componentstatuses          # Check health of cluster components
```

---

 **2. Get Resources**

```bash
kubectl get nodes                      # List all cluster nodes
kubectl get pods                       # List pods in current namespace
kubectl get pods -n <namespace>        # List pods in a specific namespace
kubectl get all                        # Get all resources in current namespace
kubectl get svc                        # List services
kubectl get deployments                # List deployments
kubectl get events                     # View recent events (for debugging)
```

---

**3. Create / Apply Resources**

```bash
kubectl apply -f <file.yaml>           # Apply config from YAML file
kubectl create -f <file.yaml>          # Create resources from YAML
```

---

**4. Delete Resources**

```bash
kubectl delete -f <file.yaml>          # Delete from YAML file
kubectl delete pod <pod_name>          # Delete specific pod
kubectl delete svc <service_name>      # Delete a service
```

---

**5. Describe & Inspect**

```bash
kubectl describe pod <pod_name>        # Detailed info about a pod
kubectl describe svc <service_name>    # Details of a service
kubectl describe deployment <dep_name> # Details of a deployment
```

---

**6. Logs & Debug**

```bash
kubectl logs <pod_name>                # Show logs of a pod
kubectl logs -f <pod_name>             # Follow logs
kubectl exec -it <pod_name> -- bash    # SSH into a pod (if bash is supported)
```

---

**7. Rollout & Scaling**

```bash
kubectl rollout status deployment/<deployment_name>   # Check rollout status
kubectl rollout undo deployment/<deployment_name>     # Roll back deployment
kubectl scale deployment <deployment_name> --replicas=3  # Scale deployment
```

---

**8. Namespace Management**

```bash
kubectl get namespaces                 # List all namespaces
kubectl create namespace <name>        # Create a new namespace
kubectl delete namespace <name>        # Delete a namespace
```

---

**9. Context & Configuration**

```bash
kubectl config get-contexts           # Show all contexts
kubectl config use-context <name>     # Switch context (i.e., to different cluster)
kubectl config current-context         # Show current context
```

---

**10. Port Forwarding & Access**

```bash
kubectl port-forward svc/<svc_name> 8080:80     # Forward local 8080 to pod/service port 80
kubectl expose pod <pod_name> --port=80 --type=NodePort  # Expose a pod as a service
```

---

### 📄 Bonus: Get YAML of Any Resource

```bash
kubectl get pod <pod_name> -o yaml              # Full YAML of pod
kubectl get svc <svc_name> -o yaml              # YAML for service
```

---

$ kubectl get nodes -o wide

$ kubectl get svc

$ kubectl top pod   ===> pod resource utilization