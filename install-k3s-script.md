# Install K3S on the Raspberry Pi

[K3S](https://k3s.io/) is an awesome lightweight Kubernetes, perfect for running on a Raspberry Pi.

Follow the installation instructions at https://k3s.io to install k3sup on the machine you will use to manage your cluster(e.g your laptop)

### High Level Setup
Run the following commands on your laptop, or local machine.

#### Server Node
```Bash
# Server Node Setup
k3sup install --ip $SERVER --user pi

# Where #SERVER is the ip address of your master/server node
```

#### Worker Nodes
```Bash
k3sup join --ip $AGEN --server-ip $SERVER --user pi

# Where $SERVER is the ip address of our master/server node
# and $AGENT is the ip address of the worker node


