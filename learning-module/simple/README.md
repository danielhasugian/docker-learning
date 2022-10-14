# Simple

## Run Hello world
```shell
docker run hello-world
# to run image that print out 'hello world'

```
## Run nginx
```shell
docker run nginx:alpine
# to run image nginx

docker run -p 2222:80 nginx:alpine
# '-p 2222:80' publish container port 80 to host port 2222

docker run -p 2222:80 --name nginx-first-run nginx:alpine
# '--name nginx-first-run' assign name container 

docker run -p 2222:80 --name nginx-first-run --rm nginx:alpine
# '--rm' remove container if exist

docker run -p 2222:80 --name nginx-first-run --rm -d nginx:alpine
# '-d' run in background

docker run --help
# print run --help

docker exec -it nginx-first-run ash
touch /usr/share/nginx/html/index.html
cat > /usr/share/nginx/html/index.html << EOF 
  <html><body> Hello world</body></html> 
EOF
# 'exec -it nginx-first-run ash' Entering container with ash (unix shell)
# 'touch ..' Create file index.html
# 'cat > ..' Write value into index.html

```

## Run nginx with Dockerfile
With sample file nginx/index.html & nginx/Dockerfile
```shell
docker build nginx/ -t nginx-custom -f Dockerfile
docker run -d -p 3333:80 nginx-custom
```


## Create sample log-event 
```shell
docker build log-event/ -t i-log-event
docker run i-log-event cat log.txt
#'Run' is executed when image build time.
#'Entry point' is executed when container is starting
```


