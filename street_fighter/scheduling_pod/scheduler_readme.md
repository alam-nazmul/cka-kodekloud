#### Scheduler is responsible for Up and running a Pod in which node depending on Node's resources and other parameters.

#### If the scheduler goes down, the existing Pods will run as before.


### Scheduling:
1. Manual scheduling
2. NodeSelector
3. Node affinity


### Manual scheduling:
For Manual scheduling, we will define the node name on Pod definition file.

### NodeSelector:
For NodeSelector, pod will schedule by their Node's labels. So, we need to create the labels on nodes.



#### Labels are working as tag
#### Selectors are working as a filter with Labels
#### You can add as many labels as you like.


### How to get nodes labels
```Actionscript
kubectl get nodes --show-labels
```

### How to find labels in nodes
```Actionscript
kubectl get nodes --selector <label_name>=<label_value>
```


