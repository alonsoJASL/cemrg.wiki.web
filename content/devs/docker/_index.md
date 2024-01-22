---
# Title, summary, and page position.
linktitle: CemrgApp + Docker
summary: Learn the about Docker on CemrgApp.
weight: 3
icon: book
icon_pack: fas

# Page metadata.
title: Configure Docker in CemrgApp
date: '2018-09-09T00:00:00Z'
type: book # Do not modify.
---

To run all of CemrgApp's specialised modules, such as the machine learning pipeline for scar quantification, 
[Docker](https://www.docker.com) is required to be installed on the user's computer. 
We also use Docker to expand and collaborate with other centres' software.

Download Docker
---------------
Docker can be downloaded or installed from:

- [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu) for Linux.
  - You need to provide access to Docker by following these [instructions](https://docs.docker.com/install/linux/linux-postinstall), or see below for a summarised version of the instructions.
  - WARNING: this will give root access to Docker containers.
- [Docker](https://docs.docker.com/docker-for-mac/install) for macOS.
  - Simple installation and running.
- [Docker](https://docs.docker.com/docker-for-windows/install) for Microsoft Windows.


> Install docker whether it is windows, linux or macOS. Use the links on the left.

Test your configuration
-----------------------
Before running CemrgApp for the first time, run the following two commands in the terminal:

`docker pull biomedia/mirtk:v1.1.0`<br>
`docker pull orodrazeghi/cemrgnet`

Both commands will ensure the machine has access to all the necessary external software to run the CemrgApp specialised modules. The first command gets the Docker container for all the MIRTK libraries we employ, while the second command gets the Docker container for our in-house automatic segmentation machine learning model.

The time downloading varies with the internet connection. In general, it should not take more than 10 minutes from start to finish. Such process looks as shown below:

<!-- [[/Images/CemrgAppDocker.gif]] -->