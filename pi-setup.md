# Guide to Pi Setup 

## General Setup for Each Raspberry Pi

1) Burn [Raspbian Lite](https://www.raspberrypi.org/downloads/raspbian/) to SD Card using [Etcher](https://www.balena.io/etcher/)

2) Create an empty file called 'ssh' on the root of the SD card.  This will allow you to immediately connect to the Pi over ssh when it boots the first time.

3) ssh pi@raspberrypi (or IP address)
   - Had to get ipaddress first?
   - Recommend connecting to a monitor if you have issues
   - Also had to start twice?

4) sudo raspi-config
   - Set name of pi
   - Expand filesystem
   - Change password

5) sudo reboot

6) install Docker

   ```bash
   curl -sSL get.docker.com | sh && \
    sudo usermod pi -aG docker \
    newgrp docker
    ```

   ** id -aG should show groups, but not sure pi joined
   ** docker - version

7) Disable the swapfile
   - Commands
   - Verify with swapon -s

8) Edit /boot/cmdline.txt
   
9)  IMPORTANT:  sudo reboot

10) Install Kubernetes 
   curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add - && echo "deb http://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list && sudo apt-get update -q && sudo apt-get install -qy kubeadm 

12) Join the cluster