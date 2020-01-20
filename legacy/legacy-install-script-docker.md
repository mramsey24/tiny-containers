# Install Docker on a Raspberry Pi

```bash
# Execute docker install script and add pi user to docker global group
curl -sSL get.docker.com | sh && sudo usermod pi -aG docker

# Switch to the docker group
newgrp docker

# Verify Docker is installed
docker --version
```
