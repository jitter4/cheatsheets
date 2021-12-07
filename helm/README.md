# helm
## repo
### add
helm repo add stable \<repo_url\>

helm repo add stable https://kubernetes-charts.storage.googleapis.com/
#### jetstack
helm repo add jetstack https://charts.jetstack.io

### update
helm repo update

## install
helm install my-nginx stable/nginx-ingress --set rbac.create=true 