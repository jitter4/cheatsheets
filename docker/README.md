# Docker

## Attach
docker attach <container_id>

## push
docker push \<docker_id\>/\<project_name\>

## Version
docker version

## Run
### hello-world
docker run hello-world
### redis
docker run redis

docker run -it redis

docker run -p <machine-port>:<container_port> <container_id>
  
docker run -p 8080:8080 shubham01/simpleweb

### busybox
docker run busybox echo hi there

docker run busybox ls

### npm test
docker run abd0d43c81d7 npm run test -- --coverage

### -v
docker run -p 3000:3000 -v $(pwd):/app <image_id>
#### node_modules
docker run -p 3000:3000 -v /app/node_modules -v $(pwd):/app 5f4b822436a3
#### ruby
docker run -it -v $(pwd):/app ruby:2.3 sh


## PS
##3 list running containers
docker ps

## list all containers ever created
docker ps --all
### view only container id
docker ps -a -q


## Create
docker create hello-world

docker create -it hello-world

## Start
### print o/p on terminal
docker start -a <container_id>

### not print o/p on terminal
docker start <container_id>

## Logs
docker logs <container_id>

## prune
docker system prune
docker system prune -a

## Remove
docker rm $(docker ps -a -q)

## Stop - SIGTERM
docker stop <container_id>
#### stop all running containers
docker stop $(docker ps -a -q)


## Kill - SIGKILL
docker kill <container_id>

## Exec
docker exec -it <container_id> <command>
### windows - winpty - redis-cli
winpty docker exec -it <container_id> redis-cli
#### t to pretify o/p 
docker exec -i <container_id> <command>
### shell access
docker exec -it <container_id> sh
### run test
docker exec -it 80f852b05ceb npm run test

## stop & remove
docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q)

## build
docker build <parent_of_dockerfile>

docker build -t <docker_id>/<project_name>:latest .

## commit
docker commit -c 'CMD ["<<command>>"]' <container_id>

# Compose
## version
docker compose -v
## build
docker-compose build
## up
docker-compose up
## background up
docker-compose up -d
## down
docker-compose down


docker stop $(docker ps -a -q)
docker system prune -a