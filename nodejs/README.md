# Basic NodeJS Application for use in Docker and Kubernetes Examples

## Build the Container Image
```
$ docker build -t kubia .
```

## Run the Container
```
$ docker run --rm --name kubia-container -p 8080:8080 -d kubia
```
## Verify the Container is taking requests on http 8080
```
$ curl http://localhost:8080
```
## Connect to the Running Container
```
$ kubectl exec -it kubia-container bash
```
## Check Processes
```
$ ps aux | grep app.js 
```
## Stop the Container
```
$ docker stop kubia-container
```
## Remove the Container
```
$ docker rm kubia-container
```

## Pushing the Image to an Image Registry
```
docker tag kubia-container nickbaynhamdevops/kubia-container:latest
docker push nickbaynhamdevops/kubia-container:latest
```

