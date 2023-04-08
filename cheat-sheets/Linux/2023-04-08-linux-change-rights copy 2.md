---
layout: post
title: Linux change rights
date: 2023-04-08 16:29 +0200
categories: [Cheat sheets, Linux]
tags: [cheat sheets, user rights] 
---
## Changing file properties
### Changing ownership of a folder
```shell
# Change ownership on a folder to user name and user group and do it recursively
sudo chown UserName:UserGroup -R <Folder name>
```
### Marking a file executable
```shell
sudo chmod +x <file name>
```
