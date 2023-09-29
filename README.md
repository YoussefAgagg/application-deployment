# docker compose for services in https://github.com/YoussefAgagg/cloud-native-projects
########
# 7 Kubernetes fundamentals for Spring Boot
to run a PostgreSQL database
```bash
kubectl apply -f ./k8s/platform/developmen/services
```
```bash
kubectl get deployment
```
to delete
```bash
kubectl delete -f ./k8s/platform/developmen/services
```
```bash
minikube image load edge-service --profile bookshop
```
# Managing external access with Kubernetes Ingress
create profile
```bash
minikube start --cpus 2 --memory 4g --driver docker --profile bookshop
```
```bash
minikube addons enable ingress --profile bookshop
```
```bash
kubectl get all -n ingress-nginx
```
A namespace is “an abstraction used by Kubernetes to support isolation of groups of resources within a single cluster. Namespaces are used to organize objects in a cluster and provide a way to divide cluster resources” (https://kubernetes.io/docs/reference/glossary).
```bash
 minikube ip --profile bookshop
```
```bash
minikube image load edge-service --profile bookshop
```
```bash
minikube image load order-service --profile bookshop
```
```bash
minikube image load config-service --profile bookshop
```
```bash
minikube image load catalog-service --profile bookshop
```
On macOS and Windows, the ingress add-on doesn’t yet support using the minikube cluster’s IP address when running on Docker. Instead, we need to use the `minikube tunnel --profile bookshop` command to expose the cluster to the local environment, and then use the 127.0.0.1 IP address to call the cluster. This is similar to the `kubectl port-forward` command, but it applies to the whole cluster instead of a specific service.
- in root dir of service run
```bash
kubectl apply -f k8s
```
```bash
kubectl get ingress
```
```bash
minikube tunnel --profile bookshop
```
```bash
minikube stop --profile bookshop
```
```bash
minikube start --profile bookshop
```
```bash
 minikube delete --profile bookshop
```
to run in windows disable IIS Web Server
# Rabbitmq 
```bash 
docker-compose up -d bookshop-rabbitmq
```
[rabbitmq](http://localhost:15672)