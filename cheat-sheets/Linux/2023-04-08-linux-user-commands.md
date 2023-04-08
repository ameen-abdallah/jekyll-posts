---
layout: post
title: Linux user commands
date: 2023-04-08 16:30 +0200
categories: [Cheat sheets, Linux]
tags: [cheat sheets, user commands]
---
## Some basic user commands
### Adding a user
```shell
sudo adduser user1
```
### Deleting a user
```shell
sudo userdel -r ‘user1’
```
### Change password
```shell
sudo password user1
```
### Adding a user to a group
```shell
sudo usermod -a -G groupa user1
```
### Deleting a user from group
```shell
sudo deluser user1 groupa
```