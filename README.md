# Mac OS Ventura on Dell Latitude E7470 using Opencore
- Mac OS Ventura 13
- Opencore 0.9.4

![opencore](https://github.com/vpcano/Hackintosh_OC_Ventura_LatitudeE7470/assets/15021507/9d062c19-6aba-49f3-9c42-51e0fe3ed6e5)

## Features
* [x] Everything seems to work fine (display, graphics acceleration, sleep and wake, speakers, keyboard and trackpad...)
* [x] USB mapping done (including dock station USB ports)
* [x] WIFI + Bluetooth working with default Intel card*

*: In order for continuity functions (such as Airdrop) to work, you will need to replace stock Intel wireless adapter with a M.2 A+E adapter using one of the following chipsets:
- BCM943602
- BCM94360
- BCM94352
- BCM94350

See [Wireless Buyers Guide](https://dortania.github.io/Wireless-Buyers-Guide/) for more info.

*TODO*: in that case, config.plist should be edited in order to enable required kexts

## Installation
1. Clone this repository and take the *EFI* folder
2. Format an USB flash drive using FAT32 format, download a copy of a mac OS Ventura recovery following [this tutorial](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/), and place it on the root of the flash drive
3. Place the EFI folder on the root of the flash drive
4. Enter BIOS settings (pressing F2 key) and do the following tweaks:
   - Disable Fastboot
   - Disable Secureboot
   - Disable Serial Port
   - Disable Parallel Port
   - SATA Mode: AHCI
   - Put your flash drive on the top of the boot sequence
5. Boot from your flash drive and once the Opencore boot selector appears select the recovery option
6. Wait until you see Mac OS Ventura recovery
7. Make sure you have an internet connection. If Wifi is unavailable, just use a wired connection
8. Enter Disk Utility and format your internal drive using APFS format
9. Install macOS Ventura. The laptop may reboot several times, don't take out the USB flash drive at any moment.
10. Once you get your macOS fresh install, you will need to be able to [boot without the USB](https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html). Use [MountEFI](https://github.com/corpnewt/MountEFI) or a similar tool to mount your drive's EFI partition, and place the EFI folder from the USB on it.
11. Shutdown, take out the USB, and enjoy your Hackintosh

## Based on
- [Opencore official website](https://dortania.github.io/)
- [OS X Latitude forum](https://osxlatitude.com/forums/topic/9179-dell-latitude-e7x70-clover-and-opencore/#comment-104256)
