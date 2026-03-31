---
description: How to turn an old PC into golden deliciuos butter!
---

# PC/Laptop Support (BETA!)

An important new development for the ButterBox project is the ability to turn any Intel or AMD 64-bit PC into a ButterBox. In many places in the world, getting access to an official RaspberryPi is difficult and expensive. However, no matter where you are in the world, there seem to be plenty of "old", unloved, discarded PC towers and laptops.

This page will help you bring new life to that old tech, by turning it into the best kind of buttery local microserver, that even has a built-in battery, screen and keyboard!

## Download the Image

Access to new images of ButterBox built for Intel/AMD64 devices are now available IN EARLY BETA through our [development image distribution site](https://files.sr2.uk/d/52bd8561a10d4d83be7b/?p=%2F&mode=list). Download the latest image that beings with "amd64_butter_main_".

## How to Flash

This image can be flashed to a bootable USB drives, using [balenaEtcher](https://etcher.balena.io/).

1. Install balenaEtcher
2. Download the AMD64 image and unpack it (remove .tar and .gz with "unzip" tool)
3. Select the image file in balenaEtcher
4. Plugin the USB flash drive
5. Select the drive in balenaEtcher
6. Flash!

## How to Boot Up

Once the USB drive is flashed, you can now use it to boot up ButterBox on your old PC. 

1. Boot your old PC into the "BIOS" screen. Make sure it is configured to allow for booting from the USB drive, before it boots the internal hard drive.
2. Shutdown the PC.
3. Plug in the USB drive to the PC
4. Start the PC, and make sure it boots from the USB drive.
5. Wait for the login terminal to appear!

## How to Access

Once the ButterBox PC is booted up, and plugged into a local router, it should be ready to access!

Connect your personal device to the same network, and try to access [http://butterbox.local](http://butterbox.local)
 
## Differences from RaspberryPi edition

There are some important differences between ButterBox on PC versus on RaspberryPi

- There is no built-in wifi hotspot. You must plug it into a dedicated wifi router or network.
- You can easily access the terminal "root" user to update and configured (with great power, comes great responsibility!)


