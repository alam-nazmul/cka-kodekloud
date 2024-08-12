### Update the hosts file
```
vim /etc/hosts
    172.16.7.235	kmaster1
    172.16.7.236	kworker1
    172.16.7.237	kworker2
```

### Add GPG key
```
curl -fsSL https://pkgs.k8s.io/core:/stable:/v1.30/deb/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg
```


### Update the source file
```
echo 'deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.30/deb/ /' | sudo tee /etc/apt/sources.list.d/kubernetes.list
```

### Update the all packages
```
apy update -y
```

### Install Kubernetes Tools
```
apt install kubeadm kubelet -y
```


### Check the kubeadm version
```
kubeadm version
```

### Check theu Kubelet version
```
kubelet --version
```

### Disable the swap space. Also remove the swap entry from '/etc/fstab'
```
swapoff -a
```


### Load the required modules
```
vim /etc/modules-load.d/k8s.conf
    overlay
    br_netfilter
```


### Reload the modules
```
modprobe overlay
modprobe br_netfilter
```


### Check the module status
```
lsmod | grep over
lsmod | grep br_netfilter
```


### Enable the ip forwarding
```
vim /etc/sysctl.d/10-k8s.conf
    net.bridge.bridge-nf-call-ip6tables = 1
    net.bridge.bridge-nf-call-iptables = 1
    net.ipv4.ip_forward = 1
```

### Reload this configuration
```
sysctl --system
```

### Check the docker driver. If  "Cgroup Driver: systemd", then it's okay.
```
docker info | grep -i driver
```


###  If "Cgroup Driver: cgroup" then change it by below cmd
```
vim /etc/default/kubelet
    KUBELET_EXTRA_ARGS="--cgroup-driver=cgroupfs"
```

### Reload the daemons
```
systemctl daemon-reload
```


### Restart the kubelet service
```
systemctl restart kubelet.service
```

### Remove the '/etc/containerd/config.toml'
```
rm -rf /etc/containerd/config.toml
```


### Restart the containerd service
```
systemctl restart kubelet.service
```

### Enter the token cmd line, which we previously get from master node
```
kubeadm join 172.16.7.235:6443 --token 3bimht.7jw6lzjpuqmiuyzb \
	--discovery-token-ca-cert-hash sha256:5fa1aec6f7db2a6f738425a0b54a77821f16baf6c343cfe988646ef79a3f0bbc
```

### Check the all pods
```
kubecrl get pods -A -o wide
```
