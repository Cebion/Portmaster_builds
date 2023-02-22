# PortMaster - Builds

This repository provides compile instructions for each port and how to setup the build environment used by me for my Ports.

# Build Environment

My current build environment is a chroot inside an Ubuntu 20.04 WSL2.

Instructions how to set it up:

Install required packages on Ubuntu 20.04 LTS WSL 2
```
sudo apt install \
build-essential \
binfmt-support \
daemonize \
libarchive-tools \
qemu-system \
qemu-user \
qemu-user-static \
gcc-aarch64-linux-gnu \
g++-aarch64-linux-gnu
```
- Download 20.04 Focal server-cloudimg-arm64-wsl.rootfs.tar.gz from Ubuntu Cloud image. https://cloud-images.ubuntu.com/releases/

- Extract the tarball in a folder:

```
mkdir folder
sudo bsdtar -xpf ubuntu-20.04-server-cloudimg-arm64-wsl.rootfs.tar.gz -C folder
```

- Copy qemu static binary into that folder:

```
sudo cp /usr/bin/qemu-aarch64-static folder/usr/bin
```

- Start systemd with daemonize:
```
sudo daemonize \
/usr/bin/unshare -fp --mount-proc \
/lib/systemd/systemd --system-unit=basic.target
```

- Check if AARCH64 binfmt entry is present:
```
ls /proc/sys/fs/binfmt_misc/
```

- Mount and chroot into the environment:
```sudo mount -o bind /proc folder/proc
sudo mount -o bind /dev folder/dev
sudo chroot folder qemu-aarch64-static /bin/bash
```

- In the chroot, delete /etc/resolv.conf file and write a name server to it.
```rm /etc/resolv.conf
nameserver 8.8.8.8
```
- Exit chroot 
- Create chroot.sh

```#!/bin/bash

sudo daemonize \
/usr/bin/unshare -fp --mount-proc \
/lib/systemd/systemd --system-unit=basic.target

sudo mount -o bind /proc folder/proc
sudo mount -o bind /dev folder/dev
sudo chroot folder qemu-aarch64-static /bin/bash
```
- Update & Upgrade the chroot
```
apt-get update && apt-get upgrade 
```

- Helpful development tools & libraries to have in the chroot

```
apt -y install build-essential git wget libdrm-dev python3 python3-pip python3-setuptools python3-wheel ninja-build libopenal-dev premake4 autoconf libevdev-dev ffmpeg libboost-tools-dev magics++ libboost-thread-dev libboost-all-dev pkg-config zlib1g-dev libsdl-mixer1.2-dev libsdl1.2-dev libsdl-gfx1.2-dev libsdl2-mixer-dev clang cmake cmake-data libarchive13 libcurl4 libfreetype6-dev librhash0 libuv1 mercurial mercurial-common libgbm-dev libsdl-image1.2-dev
```


- Install custom SDL2 Libraries for better compatiblity
wget https://github.com/libsdl-org/SDL/archive/refs/tags/release-2.26.2.tar.gz

```
./configure --prefix=/usr
```

Important that you don't install libsdl2-dev package.

