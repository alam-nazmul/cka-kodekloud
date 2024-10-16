#### NodePort builds on top of the ClusterIP Service and provides a way to expose a group of Pods to the outside world. At the

#### API level, the only difference from the ClusterIP is the mandatory service type which has to be set to NodePort , the rest of the values can remain the same.

#### ClusterIP Services allow internal connectivity between different applications within the cluster, providing a stable IP address for communication.


### NodePort range: 30000 - 32767


### How to create a NodePort
```angular2html
kubectl create service nodeport <nodeport_name> --tcp <service_port>:<container_port> --node-port <nodeport_port>
```