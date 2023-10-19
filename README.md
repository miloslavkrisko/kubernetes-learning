# kubernetes-learning

# Usefull Links

https://kubernetes.io/docs/home/

# Commands

# # Kubernetes Commands 
# # # Configmap
```
cd config
kubectl create configmap --from-file=app.properties file-conf --dry-run=client -o yaml >> file-conf.yaml
kubectl create configmap env-conf --from-literal=OS_VAR=VALUE --dry-run=client -o yaml >> env-conf.yaml
```

# # # Secret

# # # Deployment

# # # Statefulset

# # # Daemonset

# # # Cronjob

# # # Pod


# # Helm command
```
helm create <FolderName>
helm create example 
```
