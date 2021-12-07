# terraform

## init
terraform init

## apply
terraform apply
terraform apply -var="region=us-east-1"
terraform apply -var-file="sensitive.tfvars"
terraform apply -var 'amis={ us-east-1 = "foo", us-west-2 = "bar" }'

## show - to get current state
terraform show

## destroy - tear down resources
terraform destroy

## unset
unset TF_VAR_region