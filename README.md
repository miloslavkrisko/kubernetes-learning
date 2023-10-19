# kubernetes-learning

## Links
https://kubernetes.io/docs/home/

https://helm.sh/docs/

## Plugins & Tools
1. VS Code
Plugins:
- vscode-helm
- helm extras
- docker
- aws toolkit


# Commands

## Kubernetes Commands 
### Configmap
```
cd config
kubectl create configmap --from-file=app.properties file-conf --dry-run=client -o yaml >> file-conf.yaml
kubectl create configmap env-conf --from-literal=OS_VAR=VALUE --dry-run=client -o yaml >> env-conf.yaml
```

### Secret

### Deployment

### Statefulset

### Daemonset

### Cronjob

### Pod


## Helm command
```
helm create <FolderName>
helm create example 
helm upgrade --install --dry-run <ReleaseName> -f values.yaml -f values-<env>.yaml ./

# Usefull command for generating the structure to know if there isnt any syntax error or missplacement
helm template --debug
```
