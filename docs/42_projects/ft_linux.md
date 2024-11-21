# Ft_Linux

## Introduction

Welcome to ft_linux. In this subject, you have to build a basic, but functional, linux
distribution.

This subject is not about Kernel programming, but it’s highly related.
This distro will be the base for all your kernel projects, because all your kernel-code will
be executed here, on your distro.
Try to implement what you want/need to. This is your userspace, take care of it!

## Goals

- [x] Build a Linux Kernel
- [x] Install some binaries (See the list below)
- [x] Implement a filesystem hierarchy compliant with the [standards](http://refspecs.linuxfoundation.org/FHS_3.0/fhs/index.html)
- [x] Connect to the Internet

## General instructions

### The links

- [The Bible](http://www.linuxfromscratch.org/lfs/view/stable/index.html)
- [How to build a Kernel](https://old-en.opensuse.org/Configure,_Build_and_Install_a_Custom_Linux_Kernel)
- [Autotools](https://www.gnu.org/software/automake/manual/html_node/index.html#SEC_Contents)

### Instructions

- [x] For this subject, you must use a virtual machine, live VirtualBox or VMWare.
  > Though it is not REQUIRED, you SHOULD read [this](https://pubs.opengroup.org/onlinepubs/9699919799/) and [that](http://refspecs.linuxfoundation.org/lsb.shtml) right now.
  > Keep those standards in mind. You won’t be graded on your compliance with them, but still, it would be good practice.
- [x] You must use a kernel version 4.x. Stable or not, as long as it’s a 4.x version.
- [x] The kernel sources must be in /usr/src/kernel-\$(version)
- [x] You must use at least 3 differents partitions. (root, /boot and a swap partition).
  > You can of course make more partitions if you want to.
- [x] Your distro must implement a kernel_module loader, like udev.
- [x] The kernel version must contain your student login in it. Something like ‘Linux kernel 4.1.2-<student_login>‘
- [x] The distribution hostname must be your student login
- [x] You’re free to choose between a 32 or 64-bit system.
- [x] You must use a sofware for central management and configuration, like SysV or SystemD.
- [x] Your distro must boot with a bootloader, like LILO or **GRUB**.
- [x] The kernel binary located in /boot must be named like this: vmlinuz-<linux_version>-<student_login>. Adapt your bootloader configuration to that.

### Prerequis du systeme hote

    - OK (voir version-check.sh)
    - Add controleur SATA 20G pour LFS
    - New partitions (voir fdisk + cfdisk)
    	- Size, type(L)
    	- Creation systeme de fichier sur partition
    	- Monter partition avec point de montage

    - Telechargement paquets (374 Mo)

### Commandes utiles

    - blkid (UUIDs de chaque partion)
    - fdisk / cfdisk
    - mkfs -v -t ext4 /dev/<xxx>
    - mkswap /dev/<yyy>
    - mount

### Fichiers utiles

    - /etc/fstab
    - /etc/mtab
