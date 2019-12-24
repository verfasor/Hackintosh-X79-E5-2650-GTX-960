[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/mighil)

**DISCLAIMER: YOU'RE NOTHING BUT AN A-HOLE IF YOU SELL EFI FOLDER (CONFIG) THAT'S ALREADY AVAILABLE FOR FREE OF COST. DON'T DO THAT.**

## X79/LGA2011 Hackintosh High Sierra EFI for E5-2650 & GTX 960.

Fork or star, it's your call. You need to modify a lot if your system specs are different. I use an Ant Country chinese motherboard. Very similar to Huanan X79. You can refer to this guide if you've a Huanan X79 mobo.

Also note that I've set my system memory info within the SMBIOS in clover. You should edit that.

![X79 E5-2650 Hackintosh!](https://res.cloudinary.com/mighil/image/upload/v1577167911/hackintosh-x79-e5-2650-gtx-960_t2qd5y.png)


## #README

- Proceed with caution.
- Kindly delete the VoodooHDA from **kexts/Other** if AppleALC is working.
- N/A for Opencore bootloader. Go ahead though, if you know what you're doing. 
- I haven't tested these settings against the latest version of Clover. 

The EFI folder is applicable for Vanilla approach and SSD hot-swap (just replace/paste EFI folder - not recommended though.) Use [this EFI](https://olarila.com/forum/viewtopic.php?t=10596) if mine isn't working. But then you'll to tweak a lot.

## What Doesn’t Work?

- Sleep/wake
- FaceTime/iMessage (maybe, haven't tested yet though)

I've used [neofetch](https://github.com/dylanaraps/neofetch) to display system specs via Terminal.

## Resources

- [Guide to install High Sierra](https://hackintosher.com/guides/high-sierra-install-full-guide/)
- [Guide to make High Sierra USB Installer](https://hackintosher.com/guides/make-macos-flash-drive-installer/)

## Post USB preparation

1. Use Clover Configurator (macOS) or DiskGenius (Windows) to mount the EFI folder within USB installer. 
2. Paste my folder to the EFI partition.

## Prepare motherboard for macOS installtion

- Disable Intel® Virtualization Technology (Intel® VT)

## Post Installation

1. Copy Lilu.kext and WhateverGreen.kext from EFI/Clover/Kexts/Other to Libray/Extensions and reboot.
2. Use this command in terminal to install Nvidia Webdrivers for GTX 960. `bash <(curl -s https://vulgo.github.io/webdriver) 387.10.10.10.40.113`
