# k3s-getting-started

## Install

curl -sfL https://get.k3s.io | sh -

#### Check for Ready node, takes maybe 30 seconds
  k3s kubectl get node
  
  
## Deploy Test Container

kubectl create deployment app1 --image u1ih/hello

## List Deployments

kubectl get deployments

## Create a Service for the App
kubectl expose deployment/app1 --type="NodePort" --port 8080

or

kubectl expose deployment/app1 --type="LoadBalancer" --port 8080


## List Services

kubectl get svc

## Access the Service

curl <IP>:8080
