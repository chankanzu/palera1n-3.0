# 
![palera1n-Header](https://user-images.githubusercontent.com/104146035/204871654-854b47a5-866b-41e1-aaab-8059cbfc4b9a.jpg)






# This is a work in progress. by [pwnd2e@Twitter](https://twitter.com/pwnd2e) for this modified version of [palera1n](https://github.com/palera1n/palera1n)
Read this throughly, feel free to ask questions, know the risks. 

- 1. [open](https://discord.gg/5pWry9wn6p) Ask in r/jailbreak Discord #palera1n channel
- 2. [open](https://discord.gg/4S3yUMxuQH) Ask in palera1n Discord
- 3. [open](https://discord.gg/kKJmDDaZrB) Ask in 2escustomservices Discord #palera1n channel
- 4. Or open a GitHub issue

Please, please, please, provide necessary info:

- iOS version and device (eg. iPhone 7+ 15.1, iPhone 6s 15.3.1)
- Computer's OS and version (eg. Ubuntu 22.04, macOS 12.0 and up)
- The command you ran
- Debug logs with `--debug`



# palera1n

iOS 15.0-15.7.1 **work in progress, tethered** checkm8 "jailbreak" 

# What does this do?

It boots the device with AMFI patches. On first run, it'll boot a ramdisk which dumps your onboard blob, and installs Sileo and Substitute.

**WARNING 1**: I am NOT responsible for any data loss. The user of this program accepts responsibility should something happen to their device. While nothing should happen, jailbreaking has risks in itself. If your device is stuck in recovery, please run `futurerestore --exit-recovery`, or use `irecovery -n`. Using this on iOS 16 has a higher chance of bootlooping you.

On A10 and A11, you **must disable your passcode while in the jailbroken state**. On A10, this can be fixed in the future by implementing blackbird. On A11, we don't have a SEP exploit yet.

# Linux issues
Linux has some weird usbmuxd issues. We have tried our best to fix them, but there stil are issues. We highly recommend to compile and install [usbmuxd2](https://github.com/tihmstar/usbmuxd2).

Stop making issues about Linux not being able to connect, we are aware. This includes being stuck on waiting for ramdisk to finish booting.

# Prerequisites
- 1. checkm8 vulnerable iOS device on iOS 15 (A8X-A11)
    - You must install the Tips app from the App Store before running the script
- 2. Linux or macOS computer
    - Python 3 is required
- 3. iOS 15.0-15.7.1
- 4. A brain
    - Remember, this is mainly for developers.

# How to use
- 1. Clone this repo with `git clone --recursive https://github.com/pwnd2e/palera1n-3.0 && cd palera1n-3.0`
    - \[A10+\] Before running, you **must** disable your passcode
    - Put your device in DFU Mode before running.
- 2. - For rootless Run `./palera1n.sh --tweaks <ios version youre on atm>`   
   _for fakefs run `./palera1n.sh --tweaks <ios version youre on atm> --semi-tethered` 
   - With semi-tether after first install and re-jailbreaking just hit activate tweaks then respring
   - if your having trouble with dfu booting in the middle of the procces,
     start over and use   `./palera1n.sh --dfuhelper` 
when it starts ramdisk exit out of terminal and cd back into palera1n and start from 2 again.
    - You will be prompt do you unerstand type  `Yes, pwn my idevice`  
    - then it will ask you again type `Yes, do as I say`
- 3. Let it ra1n







# Repos
All repos work because it uses normal Procursus and not rootless.
- [pwnd2e](https://www.2escustomservices.com/iOS15) You can add this repo for tweaks that wont bork your idevice

# Credits


- [pwnd2e](https://github.com/pwnd2e) for this modified fork

- [Nathan](https://github.com/verygenericname)
    - The ramdisk that dumps blobs is a slimmed down version of SSHRD_Script
    - Also helped Mineek getting the kernel up and running and with the patches
    - Helping with adding multiple device support
- [Mineek](https://github.com/mineek)
    - For the patching and booting commands
    - Adding tweak support
- [Amy](https://github.com/elihwyma) for the Pogo app
- [nyuszika7h](https://github.com/nyuszika7h) for the script to help get into DFU
- [the Procursus Team](https://github.com/ProcursusTeam) for the amazing bootstrap
- [F121](https://github.com/F121Live) for helping test
- [tihmstar](https://github.com/tihmstar) for pzb/original iBoot64Patcher/img4tool
- [xerub](https://github.com/xerub) for img4lib and restored_external in the ramdisk
- [Cryptic](https://github.com/Cryptiiiic) for iBoot64Patcher fork


