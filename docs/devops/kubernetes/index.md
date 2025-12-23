---
title: Kubernetes
tags:
  - devops
  - kubernetes
  - k8s
---

# Kubernetes Notes

Container orchestration with Kubernetes.

## Topics

- [ ] Core concepts (Pods, Services, Deployments)
- [ ] ConfigMaps and Secrets
- [ ] Ingress and networking
- [ ] Persistent storage
- [ ] Helm charts
- [ ] Operators

---

## Quick Reference

### kubectl Commands

```bash
# Get resources
kubectl get pods
kubectl get services
kubectl get deployments

# Describe resource
kubectl describe pod <pod-name>

# Logs
kubectl logs -f <pod-name>

# Execute into pod
kubectl exec -it <pod-name> -- /bin/sh

# Apply manifest
kubectl apply -f deployment.yaml

# Delete resource
kubectl delete -f deployment.yaml

# Context management
kubectl config get-contexts
kubectl config use-context <context>
```

### Basic Deployment

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: myapp
        image: myapp:latest
        ports:
        - containerPort: 8080
        resources:
          limits:
            memory: "128Mi"
            cpu: "500m"
---
apiVersion: v1
kind: Service
metadata:
  name: myapp-service
spec:
  selector:
    app: myapp
  ports:
  - port: 80
    targetPort: 8080
  type: ClusterIP
```

---

!!! tip "Use k9s for cluster management"
    k9s provides a terminal-based UI for Kubernetes clusters.
    ```bash
    brew install k9s
    k9s
    ```
