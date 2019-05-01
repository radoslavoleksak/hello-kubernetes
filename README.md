1. Build and push hello-kubernetes docker image to dockercloud
```
$ docker login
$ docker build -t rolexak/hello-kubernetes:v3 .
$ docker push rolexak/hello-kubernetes:v3

2. run image in kubernetes cluster
```
$ kubectl run hello-kubernetes --image=rolexak/hello-kubernetes:v3 --port=9000 --image-pull-policy=Always
```