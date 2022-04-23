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
