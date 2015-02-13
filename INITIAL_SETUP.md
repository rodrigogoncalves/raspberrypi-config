# Initial setup from a fresh Arch Linux install

## Install things

```shell
pacman -Syu
pacman -S mlocate git nodejs vim-minimal sudo iputils hfsprogs gcc make
updatedb
hostnamectl set-hostname framboesa
```

## Create user

```shell
useradd -m -G wheel -s /bin/bash rodrigo
passwd rodrigo
visudo
```

# Adding swap memory for compilations

Sometimes a compilation will fail because of short memory.
For those cases it is usually enough to create a temporary swap file:

```shell
su
fallocate -l 512M /swapfile
chmod 600 /swapfile
mkswap /swapfile
swapon /swapfile
free -h
```