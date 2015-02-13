# Tips for working with the ARM Arch Linux in a Raspberry Pi

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