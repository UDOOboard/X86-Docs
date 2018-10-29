UDOO X86 is a Single Board Computer based on the N-Series Intel® Pentium® / Celeron® and x5-Series Atom family of System-on-Chips (SoCs) formerly coded as Braswell, a series of Quad Core SoCs with 64-bit instruction set and very low TDP.

Thanks to the x86_64 instruction set, the UDOO X86 supports all the x86 Android distribution for 32-bit(aka i386, IA-32, x86-32, x86_32) and 64-bit(aka x64, x86-64, x86_64).  

We suggest to always use a **64-bit** OS version.

## BlissOS - BlissOS X86 Rom for UDOO X86

This is a really useful Open-Source Android ROM for x86 based on the AOSP.

> Bliss x86 - For PC's and Laptops
This is a newer spin on Bliss for your x86 PC's, Laptops, Tablets and x86 maker boards.
Devices: Compatible with the growing number of Intel x86 CPU's This includes some AMD and Nvidia CPU's (MBR and UEFI Compatible)

Bliss-x86 is for PC project, will have a few PC centric extras added in to help with application compatibility, mouse integration, keyboard shortcuts, tc. And the creators have added a few little Linux throwbacks like bash and busybox commands, integrated Terminal and much more.  
You can also find some additional features pre-installed like Root permission (SuperSu), Houdini application compatibility (to run ARM application), TaskBar launcher for a Desktop experience, in addition to the Pico version of [OpenGapps](https://github.com/opengapps/).

### Installation

<span class="label label-warning">Heads up!</span> This is not developed by the UDOO Team so it is not official and supported directly.

You can download the official BlissRom builds for UDOO X86 in official the [download page](https://sourceforge.net/projects/blissos-x86/files/Official/udoo/).

To prepare a bootable USB with the installer you can follow the UDOO [Getting Started](https://www.udoo.org/get-started-x86/) guide or check the official [BlissRom documentation](https://forum.xda-developers.com/android/software/x86-bliss-x86-pc-s-t3534657).

On the [UDOO youtube channel](https://www.youtube.com/user/UDOOboard) you can find an installation video-guide of how to install Android Bliss-x86 on an empty drive (e.g. eMMC) of the UDOO X86. [Android Installation on UDOO X86](https://www.youtube.com/watch?v=sa84l03dq8M).

<span class="label label-warning">Heads up!</span> If during the all installation procedure you'll experience any problem with wireless mouse or keyboard, just remember to use a USB cabled mouse or keyboard instead.

<span class="label label-warning">Heads up!</span> When you boot Android Bliss-x86 for the first time (first boot takes some minutes) the Google *SetupWizard* App will start automatically, like what append in a brand new Android phone. *SetupWizard* will crash if your device doesn't have working [wifi module](!Hardware_&_Accessories/Official_Accessories).  
If you have this issue, please add `SETUPWIZARD=0` to your grub command in order to skip it.
To do this you have to stop the boot at grub and press `e` to temporarily modify the standard boot command in this way:

```
setparams `Android-x86 ...`
    search --set=root --file /android-...
    linux ... androidboot.selinux=permessive SETUPWIZARD=0 buildvariant=eng
    initrd /android-...
```

<br/>
<br/>

## Android-x86 Project - Run Android 8.1 on Your UDOO X86

From the official [android-x86.org](http://www.android-x86.org/) website:

> This is a project to port [Android open source project](http://source.android.com/) to x86 platform, formerly known as "[patch hosting for android x86 support](http://code.google.com/p/patch-hosting-for-android-x86-support/)". The original plan is to host different patches for android x86 support from open source community. A few months after we created the project, we found out that we could do much more than just hosting patches. So we decide to create our code base to provide support on different x86 platforms, and set up a git server to host it.

The last build of Android-x86 is based on Android 8.1 Oreo.

### Installation

You can download the file `android-x86_64-8.1-rc1.iso` from the official [downaload page](https://osdn.net/projects/android-x86/releases/69704).  
This is tested and perfectly working on UDOO X86.

To prepare a bootable USB with the installer you can follow the UDOO [Getting Started](https://www.udoo.org/get-started-x86/) guide, or the official [android-x86 documentation](http://www.android-x86.org/documents/installhowto).  

<span class="label label-warning">Heads up!</span> If after a complete installation Android-x86 doesn't boot properly, we suggest to prepare the partition where you want to install the OS formatting it in `ext4` and **do not** format again the partition during the Android-x86 wizard installation. This is a known issue, we found this solution in different articles, like [this one](https://techposts.org/install-android-6-marshmallow-laptop-pc/), for example.

<br/>
<br/>

## Remix OS for PC

Another one of the most famous Android projects for x86 is Remix OS.  
From the official [remixos](http://www.jide.com/remixos-for-pc) website.

> Remix OS from Jide is a reimagination of Android that provides a desktop-like windowed environment, powered by Android, to grant the benefits of the mobile OS with productivity characteristics of a desktop operating system such as a taskbar, true multi-tasking, and more. It's currently available on hardware made by Jide, such as the Remix Mini, but is also available as a bootable operating system for X86 devices.

### Installation

You can download the iso `Remix_OS_for_PC_Android_64bit` from the official [download page](http://www.jide.com/remixos-for-pc#downloadNow).
This is tested and perfectly working on UDOO X86.

To prepare a bootable USB with the installer you can follow the UDOO [Getting Started](https://www.udoo.org/get-started-x86/) guide, or the official RemixOS [video-guide for Windows users](https://www.youtube.com/watch?v=At7_g9ZXu8s).
