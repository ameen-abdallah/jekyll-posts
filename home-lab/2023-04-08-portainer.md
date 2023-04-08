---
layout: post
title: Portainer
date: 2023-04-08 16:15 +0200
categories: [Home lab, Portainer]
tags: [home lab, portainer, upgrade] 
---
## Upgrade
### Stop and remove docker image
To upgrade to the latest version of Portainer Server, use the following commands to stop then remove the old version. Your other applications/containers will not be removed.


```shell
docker stop portainer
```

```shell
docker rm portainer
```
### Get latest version
Now that you have stopped and removed the old version of Portainer, you must ensure that you have the latest version of the image locally. You can do this with a `docker pull` command:

```shell
docker pull portainer/portainer-ce:latest
```

### Deploy latest version
Finally, deploy the updated version of Portainer:

```shell
sudo docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

Current configuration:
```shell
sudo docker ps -f "id"=69843f52a433
CONTAINER ID   IMAGE                           COMMAND        CREATED       STATUS      PORTS                                                           NAMES
69843f52a433   portainer/portainer-ce:latest   "/portainer"   4 weeks ago   Up 6 days   8000/tcp, 9443/tcp, 0.0.0.0:9000->9000/tcp, :::9000->9000/tcp   portainer
```