# Guide to Pi Setup 

## General Setup for EACH Raspberry Pi

1) Burn [Raspbian Lite](https://www.raspberrypi.org/downloads/raspbian/) to SD Card using [Etcher](https://www.balena.io/etcher/)

2) Create an empty file called 'ssh' on the root of the SD card.  This will allow you to immediately connect to the Pi over ssh when it boots the first time.

3) ssh pi@raspberrypi (or IP address)
   - Had to get ipaddress first?
   - Recommend connecting to a monitor if you have issues
   - Also had to start twice?

4) sudo raspi-config
   - Set name of pi (follow a pattern)
   - Expand filesystem
   - Change password
   - Reduce video memory to 16Mb

5) sudo reboot

6) Generate an SSH key for the pi user and copy to the Pi
```Bash
ssh-keygen

ssh-copy-id pi@raspberrypi.local
```

8) Enable container features by editing /boot/cmdline.txt and add the following to the END OF THE LINE:
```cgroup_enable=cpuset cgroup_memory=1 cgroup_enable=memory```
   
9)  IMPORTANT:  sudo reboot

