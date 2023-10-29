# kubernetes-learning

## Links
https://kubernetes.io/docs/home/

https://helm.sh/docs/

https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

https://crontab.guru/


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

```
kubectl create secret generic --from-file=secretfile.yaml=app.yaml --dry-run=client -o yaml >> secret-file.yaml
kubectl create secret generic env-conf --from-literal=OS_VAR=VALUE --dry-run=client -o yaml >> secret-env.yaml
kubectl create secret docker-registry my-secret --docker-server=DOCKER_REGISTRY_SERVER --docker-username=DOCKER_USER --docker-password=DOCKER_PASSWORD --docker-email=DOCKER_EMAIL --dry-run=client -o yaml >> docker-secret.yaml

```

### Deployment

```
kubectl create deployment --dry-run=client --image=nginx:stable test -o yaml
```

### Cronjob

```
kubectl create cronjob my-job --image=busybox --schedule="*/1 * * * *" -- date
```

### Pod

### Service

```
kubectl create service clusterip cluster-service --tcp=8080:80 --dry-run=client -o yaml >> clusterService.yaml
kubectl create service nodeport nodeport-service --tcp=8080:80 --node-port=31000 --dry-run=client -o yaml >> nodeportService.yaml
```

## Helm command
```
helm create <FolderName>
helm create example 
helm upgrade --install --dry-run <ReleaseName> -f values.yaml -f values-<env>.yaml ./

# Usefull command for generating the structure to know if there isnt any syntax error or missplacement
helm template --debug
```
