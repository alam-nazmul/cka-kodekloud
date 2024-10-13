#### _The multiple containers can run in a Pod. Every pod has unique IP address._

#### _The same ports of multiple containers in a Pod can not be possible_

### Classifications of Pod
    - Single container pod
    - Multi containers pod

#### _Sidecar containers or Helper containers are exists on Multi container Pod_


### How to run a pod by command line
```Actionscript
kubectl run <Pod_Name> --image=<image_name> --port=<port_number> --labels="app=hazelcast,env=prod"
```

### How to dry-run a pod by using command line
```Actionscript
 kubectl run <Pod_Name> --image=<image_name> --dry-run=client
```

### How to check the pod status 
```Actionscript
kubectl get pods -o wide
```

### How to check details a pod
```Actionscript
kubectl details pods <pod_name>
```

### How to delete a pod
```Actionscript
kubectl delete pods <pod_name>
```

### How to check the log for a Pod
```Actionscript
kubectl logs pods/<pod_name>
```

### How to delete all pods from the default namespace
```Actionscript
kubectl delete pods --all
```

### How to check the pods in a particular namespace
```Actionscript
kubectl get pods -o wide -n <namespace_name>
```

### How to delete all pods from a namespace
```Actionscript
kubectl delete pods --all -n <namespace_name>
```

### For more details about the Pod component 
```Actionscript
kubectl explain pod
```

### How to create a pod from YAML file in a namespace
```
kubectl create -f <file_name> -n <namespace_name>
```

### How to delete a pod from YAML file in a namespace
```
kubectl delete -f <file_name> -n <namespace_name>
```


### How to update a pod from YAML file in a namespace
```
kubectl apply -f <file_name> -n <namespace_name>
```

### How to access a pod by cli
```Actionscript
kubectl exec -it <pod_name> -c <container_name> /bin/bash
```


