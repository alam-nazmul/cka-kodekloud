### Update the existing list of packages
```
apt update -y
```

### Install some prerequisite packages
```
apt install apt-transport-https ca-certificates curl software-properties-common -y
```

### add the GPG key
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

### Add the Docker repository to APT sources:
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Update the existing list of packages
```
apt update -y
```

### Install Docker
```
apt install docker-ce -y
```

### Enable and Restart the docker service
```
systemctl enable docker --now
```

### Check the docker version
```
docker --version
```