---
layout: post
title: Linux rsync
date: 2023-04-08 16:29 +0200
categories: [Cheat sheets, Linux]
tags: [cheat sheets, rsync]
---
## Basic running of rsync
### running (**dry run**)
```shell
rsync --dry-run -avz <From folder> <ssh uri to backup server:remote folder path>
```
### running
```shell
rsync -avz <From folder> <ssh uri to backup server : remote folder path>
```
