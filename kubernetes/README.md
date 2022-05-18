# kubectl

## apply
kubectl apply -f \<filename\>
### cert-manager
kubectl apply --validate=false -f https://raw.githubusercontent.com/jetstack/cert-manager/release-0.11/deploy/manifests/00-crds.yaml
### ingress mandatory
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.29.0/deploy/static/mandatory.yaml
### ingress gce load balancer
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.29.0/deploy/static/provider/cloud-generic.yaml


## create
## namespace
kubectl create namespace \<namespace_name\>
### cert-manager
kubectl create namespace cert-manager
### secret
kubectl create secret generic \<secret_name\> --from-literal \<key\>=\<value\>

                      docker-registry

                      tls

## cluster-info
kubectl cluster-info

## delete
kubectl delete -f \<config_file\>
### deployment
kubectl delete deployment \<deployment_object_name\>
## describe
kubectl describe certificates

### service
kubectl delete service \<service_object_name\>

## desribe
kubectl describe \<object_type\> \<object_name\>

## get
### all
kubectl get all
### certificates
kubectl get certificates
### deployments
kubectl get deployments
### persistent volume
kubectl get pv
### persistent volume claims
kubectl get pvc
### secrets
kubectl get secrets
### storageclass
kubectl get storageclass
### nodes
kubectl get nodes

## logs
kubectl logs \<name_of_pod\>

### pods
kubectl get pods

### services
kubectl get services

### set
kubectl set image \<object_type\>/\<object_name\> \<container_name\>=\<new_image_to_use\>

## version
kubectl version

## apiserver
kubectl proxy --address='0.0.0.0' --port=8002 --accept-hosts='.*'
curl localhost:8002

### apis
curl localhost:8002/apis

## CRD
kubectl get crd
kubectl create -f democrd1-invalid.yaml --validate=false
kubectl get democrd democrd-1 -oyaml
 

# minikube
## ssh
minikube ssh

## addons
minikube addons enable ingress

## dashboard
minikube dashboard

## docker-env
minikube docker-env

## eval
eval $(minikube docker-env)

## ip
minikube ip

## status
minikube status

## start
minikube start

## stop
minikube stop

## update-context
minikube update-context

## version
minikube version

## service-list
minikube service list
