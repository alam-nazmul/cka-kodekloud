### Major usages of kubectl command are
    - kubectl create
    - kubectl apply
    - kubectl replace
    - kubectl delete

### kubectl create:
    1. For create the newly resources
    2. If the resources are exsits then, cluster will genarate a worning.


### kubectl apply:
    1. For update the exsiting resources if any difference between the previous file.
    2. If the resources were not exsits, then it will create the resources as newly.


### kubectl replace:
    1. For replace the immutable parameters which did not done by "kubectl apply" like name of a Pod.
    2. This operation will destroy the exsiting Pods and create the resources as per new YAML file.
    3. This parameter will not operate with exsiting resources.
    4. This parameter will not create any resources as newly.


### kubectl delete:
    1. To remove the exsiting pods.