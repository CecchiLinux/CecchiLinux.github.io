---
layout: post
title: "RaspberryPi SD card backup"
date:   2018-04-20 10:40:00 +0000
category: RaspberryPi
tags: [Raspberry, Pi, Raspbian, backup, SD]
---

This is a shot guide

### Backup
```bash
df -h
sudo dd if=/dev/mmcblk0 of=~/$(echo "mySD-"`date +"%Y%m%d"`).img
```
### Restore
```bash
sudo dd bs=4M if=~/mySD-20180419.img of=/dev/mmcblk0
```
