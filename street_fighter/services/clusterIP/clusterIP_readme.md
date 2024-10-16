#### The ClusterIP provides a load-balanced IP address. One or more pods that match a label selector can forward traffic to the IP address. The ClusterIP service must define one or more ports to listen on with target ports to forward TCP/UDP traffic to containers.


#### ClusterIP services allow internal connectivity between different applications within the cluster, providing a stable Ip address for communication.

### ClusterIP parameters:
    - protocol  (TCP / UDP)
    - port  (Port on service)
    - targetPort    (Port on Pod)


### How to create a service for ClusterIP
```angular2html
kubectl create service clusterIP <service_name> --<protocal> <port>:<targetport>
```

#### _The service labels will be same as containers labels._