#### Install
arkade install openfaas --load-balancer
######Local
arkade install openfaas

####List
faas-cli list
faas-cli list -v

####Invoke
faas-cli invoke markdown

####Pull Template
faas-cli template pull

####List Languages
faas-cli new --list


faas-cli new --lang python3 hello-openfaas --prefix="<your-docker-username-here>"