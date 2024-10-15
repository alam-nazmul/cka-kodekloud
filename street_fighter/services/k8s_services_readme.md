#### In Kubernetes, a service is a method for exposing a network application that is running a one or mode Pods in your cluster.


#### Since pods are ephemeral, a service enables a group of pods, which provide specific functions (web services, image processing, etc.) tobe assigned a name and unique IP address (clusterIP). A long as the service is running that IP address, it will not change. Services also defines policies for their access.

### Types of Service
1. ClusterIP
2. NodePort
3. Loadbalancer
4. ExternalName


### ClusterIP: 
This service is responsible for application to application communication as internally in a cluster.

### NodePort:
This service is responsible for application to external communication.

### Loadbalancer:
This service is responsible for application to external communication for public cloud infra. This a replica of NodePort.

