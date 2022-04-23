## Launching the Pod
```
kubernetes create -f /root/sre-application/nodejs/manifests/pod.yaml
```
## Getting Logs
```
kubernetes logs kubia
```
## port forwarding
```
kubectl port-forward kubia 8888:8080
curl localhost:8888
```
