# Mac OS Ventura on Dell Latitude E7470 using Opencore
- Mac OS Ventura 13
- Opencore 0.9.4

## Features
* [x] Everything seems to work fine (display, graphics acceleration, sleep and wake, speakers, keyboard and trackpad...)
* [x] USB mapping done (including dock station USB ports)
* [x] WIFI + Bluetooth working with default Intel card*

*: In order for continuity functions (such as Airdrop) to work, you will need to replace stock Intel wireless adapter (the one on the image) with a M.2 A+E adapter using one of the following chipsets:
- BCM943602
- BCM94360
- BCM94352
- BCM94350

See [Wireless Buyers Guide](https://dortania.github.io/Wireless-Buyers-Guide/) for more info.

*TODO*: in that case, config.plist should be edited in order to enable required kexts

## Installation


## Based on
- [Opencore official website](https://dortania.github.io/)
- [OS X Latitude forum](https://osxlatitude.com/forums/topic/9179-dell-latitude-e7x70-clover-and-opencore/#comment-104256)
