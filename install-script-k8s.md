# Install K8S on the Raspberry Pi



```bash
# Install K8S
$ curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add - && \
  echo "deb http://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list && \
  sudo apt-get update -q && \
  sudo apt-get install -qy kubeadm


# Verify kubeadm is installed
$ kubeadm

# Verify kubectl is installed
$ kubectl
```
```bash
# Set up the Master Node (takes awhile)
sudo kubeadm init --apiserver-advertise-address=192.168.1.174

# IMPORTANT: Capture the output of this command.  It has the key you need to join the cluster
```

```bash
# Join the cluster (workers)
# This command is generated when you install K8S
# Replace the IP with the IP of your master node
 kubeadm join 192.168.1.174:6443 --token q44kc9.t6fjli2jkvrtqz1h --discovery-token-ca-cert-hash sha256:665ae675c7f19e32cd4999350cd0b54f70b4cd2429f3259d918ac1e96c630cf2
 ```
