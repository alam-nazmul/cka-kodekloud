#### _Rollout or Rollback is  possible with deployment._

#### _Deployment is one of the mechanisms for handling workloads (applications) in Kubernetes. It is managed by Kubernetes Deployment Controller._

#### _In Kubernetes, controllers are control loops that watch the state of your cluster, then make or request changes where needed. Each controller tries to move the current cluster state closer to the desired state._

#### _Deployment is an abstraction over ReplicaSet. Under the hood, Deployment creates a ReplicaSet which in turn creates pods on our cluster. As per the name, ReplicaSet is used for managing the replicas of our pods._

#### _In summary, Controller reads the Deployment spec, forwards the pod configuration to ReplicaSet and then it creates the pods with proper replicas._


### Rolling updates Deployment:
Kubernetes promises zero down time and one of the reasons behind it is Rolling Deployments. With Rolling Deployments, Kubernetes makes sure that the traffic to the pods are not interrupted when updated pods are being deployed.


### Rollback Deployment:
Rollback Deployment means, going back to the previous instance of the deployment if there is some issue with the current deployment.


### How to create a deployment by cli:
```Actionscript
kubectl create deployment <deployment_name> --image <image_name> --replicas <number_of_replicas>
```

### How to show the deployments:
```Actionscript
kubectl get deployments
```

### How to scale Deployment: 
```Actionscript
kubectl scale deploy <deployment_name> --replicas=<number_of_replicas>
```

### How to Rolling Update Deployment by cli:
```Actionscript
kubectl set image deploy/<deployment_name> <image_name>
```

### How to find the deployment version:
```Actionscript
kubectl rollout history deployemt <deployment_name> 
```

### How to check the deployment changes on a version:
```Actionscript
kubectl rollout history deploy <deployment_name> --revision=<number_of_revision>
```

### How to rollout to a specific revision version
```Actionscript
kubectl rollout undo deploy <deployment_name> --to-revision=<Revision-no>
```


