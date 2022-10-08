# Home Assistant on Kubernetes

This is a Kubernetes deployment configuration for a simple home server set up. 


## Installation

My server is running [MicroK8S](https://microk8s.io/). 

In this configuration, an environment that supports hostPath and nodePort is required. My first attempt at deployment was on minikube; I found that because the minikube installation is deployed as a container itself, it makes hostPaths and nodePorts a bit unwieldy to manage and configure.
 

Clone the repo to the k8s host:
```
git clone https://github.com/timothyquan/homeassistant
```
Configure the hostPath and nodePort in these files:
```
homeassistant_svc.yaml
homeassistant_pv.yaml
```

To create the deployment/pod, service, and volume all at once

```
cd ./homeassistant/
kubectl create -f .
```



## License
[MIT](https://choosealicense.com/licenses/mit/)