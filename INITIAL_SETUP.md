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

# Initial setup from a fresh Debian Linux install

## Hostname

```shell
sudo vi /etc/hostname
sudo vi /etc/hosts
sudo reboot
```

## User management

```shell
useradd -m rodrigo
passwd rodrigo
userdel -r pi
visudo
```

## .bashrc featuring a Raspberry Pi colored hostname
```shell
alias ls='ls --color=auto'
alias vi="vim"
PS1='\[\e[0;32m\]\u\[\e[0;34m\]@\[\e[38;5;197m\]\h\[\e[m\] \[\e[0;34m\]\w\[\e[m\] \[\e[1;32m\]\$\[\e[m\] \[\e[1;37m\]\[\e[m\]'
```
