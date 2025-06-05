# Kubernetes Learning Project

This repository contains Kubernetes manifest files and commands I practiced while following the ["Kubernetes Crash Course for Absolute Beginners"](https://www.youtube.com/watch?v=s_o8dwzRlu4) YouTube tutorial. The files demonstrate basic Kubernetes concepts including ConfigMaps, Secrets, Deployments, and Services.

## Manifest Files
- Database configuration: `mongo-config.yaml`
- Database credentials: `mongo-secret.yaml` 
- MongoDB deployment: `mongo.yaml`
- Web application: `webapp.yaml`

## Essential Kubernetes Commands

### Cluster Management
```sh
# Start Minikube cluster
minikube start --vm-driver=hyperkit

# Verify cluster status
minikube status

# Stop the cluster
minikube stop
```

### Basic Kubernetes Operations

```sh
# Get cluster information
kubectl get node
kubectl get pod
kubectl get svc
kubectl get all

# View detailed information
kubectl get pod -o wide
kubectl describe pod {pod-name}
```

### Troubleshooting
```sh
# Access application logs
kubectl logs {pod-name}

# Resolve NodePort access issues
minikube service webapp-service
```

#### Links
* mongodb image on Docker Hub: https://hub.docker.com/_/mongo
* webapp image on Docker Hub: https://hub.docker.com/repository/docker/nanajanashia/k8s-demo-app
* k8s official documentation: https://kubernetes.io/docs/home/
* webapp code repo: https://gitlab.com/nanuchi/developing-with-docker/-/tree/feature/k8s-in-hour