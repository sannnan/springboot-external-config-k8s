# Spring boot external Config - k8s

Poc done for externalizing the configuration like user pass and URL.

## Pre-Requesite

1. Install [docker](https://docs.docker.com/docker-for-windows/install/) on your system
2. Install and run [k8s](https://kubernetes.io/releases/download/) on your system


## Installation

Use the package manager (mvn) to install.

```bash
mvn clean install -DskiptTest
```
Use docker daemon to build a docker image

```bash
docker build -t {registryname}/{folder}/{imagename}:{tag} .
```
Use docker daemon to push the docker image it to local/remote registry

```bash
docker push {registryname}/{folder}/{imagename}:{tag}
```
use minikube to run k8s - specify VM type based on your OS

```bash
minikube start 
```


## Usage
once the image is pushed to a registry, change the image name in example-pod.yaml

```
image: {registryname}/{folder}/{imagename}:{tag}
```
## Deploymnet
open terminal/cmd and goto kube directory in the above cod. Run the following commands to deploy the app in k8s cluster.

```
image: {registryname}/{folder}/{imagename}:{tag}
```

## POC for MSA k8s
[sannan](https://github.com/sannnan)