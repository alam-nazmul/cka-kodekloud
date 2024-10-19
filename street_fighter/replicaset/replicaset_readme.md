#### _To ensure the HA, we can use replicaset Cause if the node goes down, the Pod can't migrate to another node._

### How to run a replicaset by a YAML file
```Actionscript
kubectl create -f <file_name>
```

### How to show the running replicaset
```Actionscript
kubectl get replicaset -o wide
```

### How to scale up the number of replicas in a replicaset
```Actionscript
kubectl scale replicaset <name_of_replicaset> --replicas <number_of_replicas>
```

#### _Replicaset identify the Pods by using their labels. If you set the number of replicas are 5 and before that you created a Pod with similar labels. Then the Replicaset will create the 5 replicas with including the single pod._


#### _In replicaset, the selector will select the labels as AND gate solution._

#### _Rollout or Rollback is not possible with replicaset._

