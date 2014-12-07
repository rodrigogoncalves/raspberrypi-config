# Initial setup from a fresh Arch Linux install

## Install things

```shell
pacman -Syu
pacman -S mlocate git nodejs vim-minimal sudo iputils hfsprogs
updatedb
hostnamectl set-hostname framboesa
```

## Create user

```shell
useradd -m -G wheel -s /bin/bash rodrigo
passwd rodrigo
visudo
```
