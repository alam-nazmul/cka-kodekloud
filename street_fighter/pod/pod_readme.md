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

### Remember we cannot edit the specifications of an existing Pod other than the below
    - Container's image
    - initContainer's image
    - activeDeadlinesSeconds
    - tolerations

### How to edit the Pod parameters with running Pod
```Actionscript
kubectl edit pod <pod_name>
```

### How to set a new container image on running Pod
```Actionscript
kubectl set image <pod_name>/<container_name> <container_name>=<new_image_name>
```

### Remember: Pod will accept the below conditions for it's naming
1. lower case letter
2. start will number or lower case letter
3. '-' will acceptable, but '_' will not acceptable
4. Never use '.' at end for naming of pod
5. Pod name will be as FQDN.

### How to copy a file from host machine to a container
```angular2html
kubectl cp <file_name> <pod_name>:<destination_path> -c <container_name>
```

### how to copy a file from a container to host machine
```angular2html
kubectl cp <pod_name>:<source_path> <destination_path>/<file_name>
```

### How to show the log for a Pod
```angular2html
kubectl logs pods <pod_name>
```

### How to show the log for a container
```angular2html
kubectl logs pods <pod_name> -c <container_name>
```

### How to show the log for a container with last 1hr
```angular2html
kubectl logs pods <pod_name> -c <container_name> --since=60m
```

### How to show the log for a container for last 10 lines
```angular2html
kubectl logs pods <pod_name> -c <container_name> --tail=10
```

### Pod restart policy
1. Never
2. Always
3. OnFailure

#### Restart policy: Never
    - If the pod complete the assigned task, then the POD will never restart.

#### Restart policy: Always
    - The pod will restart in ifinity loop if the Pod complete the task or faceing errors or if the container can not run properly.
    - By default the pod restart policy is Never

#### Restart Policy: OnFailure
    - If the service become stop, then the Pod will restart.


#### _Note: Pod will not be restarted if a container continuously restarted._  