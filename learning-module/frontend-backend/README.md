# Docker

## Command
```shell
docker build ./backend --tag dotnet-backend
docker run -p 2222:80 --name api dotnet-backend

docker build ./frontend --tag dotnet-frontend
docker run -p 3333:80 --name html dotnet-frontend

docker network create allianz-proxy
docker network connect allianz-proxy api
docker network connect allianz-proxy html

docker build ./proxy --tag dotnet-proxy
docker run -p 4444:80 --network allianz-proxy dotnet-proxy

docker run -p 2222:80 --network allianz-proxy --name api dotnet-backend
docker run -p 3333:80 --network allianz-proxy --name html dotnet-frontend
```


## With Docker compose
```shell
docker-compose build
docker-compose down
docker-compose up

docker run -d -p 5000:5000 --restart=always --name registry registry:2
#Install docker registry

docker container stop registry && docker container rm -v registry

docker-compose push
```
Validate 
- http://localhost:5000/v2/_catalog
- http://localhost:5000/v2/<tag_name>/tags/list



