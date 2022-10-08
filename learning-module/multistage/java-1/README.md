## Docker Command

Sample multi-stage

```shell
docker build . --tag hello-world-image -f Dockerfile
# to build with name 'hello-world-image'

docker images hello-world-image
# to check images

docker images hello-world-image
# to check images

docker run hello-world-image
# to run images
```

## Output
```shell
Hello World !!!
```

## Clean up
```shell
docker images hello-world-image 
# to check images

docker images rmi hello-world-image 
# to remove images
```
