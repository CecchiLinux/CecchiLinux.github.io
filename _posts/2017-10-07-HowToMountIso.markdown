---
layout: post
title:  "How to mount an ISO image in Linux"
date:   2017-10-07 10:30:00 +0000
category: Terminal_guide
tags: [iso, mount]
---

<img src="/images/dvd-cd-media639x426.jpg" width="800" height="320" />

In this guide I want to show you how to view or extract the contents of an ISO file without burn it on a cd. You don't need to install new software, your Linux distribution as already a program called **mount** to "open" the image directly under the Linux File System.

### Step 1 - Create the mount point

At first you have to create a directory where to mount the image. It's a good practice to do this under the folder "/mnt" but you can choose any one point of the File System.

``` bash
sudo mkdir /mnt/iso
```

### Step 2 - Mount the ISO

Mount the image on */mnt/iso*. In the example, my ISO file path is */home/lacb/myIso.iso* (change it with your).

``` bash
sudo mount -o loop /home/lacb/myIso.iso /mnt/iso
```

**N.B.** This will mount the ISO in read-only mode.

### Step 3 - Read the file

Now you can read the ISO contents by opening the folder /mnt/iso using your favourite *file manager* or by acceding it with terminal.

``` bash
cd /mnt/iso
```

### Step 4 - Unmount the ISO

When you finished you should unmount the ISO.

``` bash
sudo umount /mnt/iso
```
