### Kubeadm:
It's an cluster administrative tool which is responsible for lights up the cluster, add the worker nodes and remove the worker nodes.


### Kubelet:
It is responsible for start, stop and restart the Pods.

### Kubectl:
It is a command line interface that is responsible for communicate with cluster.


### To create a new token for cluster
```Actionscript
kubeadm token create --print-join-command
```
#### _This token will valid for 24hrs_