# PostmarketOS builds for Surface Pro

This repository contains nightly PostmarketOS builds for Microsoft Surface Pro devices

## Image information
Default configuration builds image with phosh and [linux-surface](https://github.com/linux-surface/linux-surface) kernel

The default user is called 'user', password is 147147 like official postmarketOS builds

## Installation

You need already installed linux distro or LiveCD (ArchLinux LiveCD or SystemRescueCD is recommended)

Download latest successful build in [Actions](https://github.com/thedanilfezlol/surface-builds/actions)

Boot to LiveCD and go to images location

ALL YOUR DRIVE CONTENTS WILL BE ERASED

'wipefs --all /dev/nvme0n1'

You need to manually partition your disk. Recommended is 512MB for EFI Partition and all remaining for root

After all done write images to partitions using dd

'dd if=BOOT_IMAGE_LOCATION of=/dev/nvme0n1p1 bs=4096'

'dd if=ROOTFS_IMAGE_LOCATION of=/dev/nvme0n1p2 bs=4096'

Then reboot device and postmarketOS should boot
