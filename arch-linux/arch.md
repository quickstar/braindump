# Installing Arch Linux

```console
# loadkeys de_CH-latin1
# timedatectl set-ntp true
```

## Partitioning
```console
# lsblk
# parted /dev/sda
(parted) mklabel gpt
(parted) mkpart ESP fat32 1MiB 513MiB
(parted) set 1 boot on
(parted) mkpart primary linux-swap 513M 3.5G
(parted) mkpart primary ext4 3.5G 100%
(parted) quit
```

## Formatting
```console
# lsblk /dev/sda
# mkfs.fat -F32 /dev/sdx1
# mkswap /dev/sdx2
# swapon /dev/sdx2
# mkfs.ext4 /dev/sdx3
```
