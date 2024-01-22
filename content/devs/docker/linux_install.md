---
title: Install Docker on Ubuntu
linktitle: Ubuntu Install
type: book
weight: 1
---

Configure Docker on Ubuntu
--------------------------
To install, run the commands outlined in [this guide](https://docs.docker.com/install/linux/docker-ce/ubuntu).
Once installed, you need to run the following commands to make sure you can run Docker from within CemrgApp (without the need for `sudo`). 

Step 1. Create the docker group: `sudo groupadd docker`

Step 2. Add your user to the docker group `sudo usermod -aG docker $USER`

run the following command to activate the changes to groups: `newgrp docker `

Step 3. Restart (or Log out and log back in) so that your group membership is re-evaluated.

Step 4. Verify that you can run docker commands without sudo. `docker run --rm hello-world`

This command downloads a test image and runs it in a container. When the container runs, it prints a message and exits.

### If things still do not work
If you initially ran Docker CLI commands using sudo before adding your user to the docker group, you may see the following error, which indicates that your ~/.docker/ directory was created with incorrect permissions due to the sudo commands.
```
WARNING: Error loading config file: /home/user/.docker/config.json -
stat /home/user/.docker/config.json: permission denied
```
To fix this problem, either remove the ~/.docker/ directory (it is recreated automatically, but any custom settings are lost), or change its ownership and permissions using the following commands:
```
sudo chown "$USER":"$USER" /home/"$USER"/.docker -R
sudo chmod g+rwx "$HOME/.docker" -R
```