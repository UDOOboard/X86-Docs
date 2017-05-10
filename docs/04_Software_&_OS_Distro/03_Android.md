UDOO X86 is a Single Board Computer based on the N-Series Intel® Pentium® / Celeron® and x5-Series Atom family of System-on-Chips (SoCs) formerly coded as Braswell, a series of Quad Core SoCs with 64-bit instruction set and very low TDP.

Thanks to the x86_64 instruction set, the UDOO X86 supports all the x86 Android distribution for 32-bit(aka i386, IA-32, x86-32, x86_32) and 64-bit(aka x64, x86-64, x86_64).  

We suggest to always use a **64-bit** OS version.

## Android-x86 Project - Run Android on Your UDOO X86

From the official [android-x86.org](http://www.android-x86.org/) website:

> This is a project to port [Android open source project](http://source.android.com/) to x86 platform, formerly known as "[patch hosting for android x86 support](http://code.google.com/p/patch-hosting-for-android-x86-support/)". The original plan is to host different patches for android x86 support from open source community. A few months after we created the project, we found out that we could do much more than just hosting patches. So we decide to create our code base to provide support on different x86 platforms, and set up a git server to host it.

### Installation

You can download the file `android-x86_64-6.0-r1.iso` from the official [downaload page](http://www.android-x86.org/download).  
This is tested and perfectly working on UDOO X86.

To prepare a bootable USB with the installer you can follow the UDOO [Getting Started](https://www.udoo.org/get-started-x86/) guide, or the official [android-x86 documentation](http://www.android-x86.org/documents/installhowto).  

<span class="label label-warning">Heads up!</span> We have noticed some issues during the installation so we suggest to choose the `Legacy` mode at boot.

<span class="label label-warning">Heads up!</span> If after a complete installation Android-x86 doesn't boot properly, we suggest to prepare the partition where you want to install the OS formatting it in `ext4` and **do not** format again the partition during the Android-x86 wizard installation. This is a known issue, we found this solution in different articles, like [this one](https://techposts.org/install-android-6-marshmallow-laptop-pc/), for example.


## Remix OS for PC

Another one of the most famous Android projects for x86 is Remix OS.  
From the official [remixos](http://www.jide.com/remixos-for-pc) website.

> Remix OS from Jide is a reimagination of Android that provides a desktop-like windowed environment, powered by Android, to grant the benefits of the mobile OS with productivity characteristics of a desktop operating system such as a taskbar, true multi-tasking, and more. It's currently available on hardware made by Jide, such as the Remix Mini, but is also available as a bootable operating system for X86 devices.

### Installation

You can download the iso `Remix_OS_for_PC_Android_64bit` from the official [download page](http://www.jide.com/remixos-for-pc#downloadNow).
This is tested and perfectly working on UDOO X86.

To prepare a bootable USB with the installer you can follow the UDOO [Getting Started](https://www.udoo.org/get-started-x86/) guide, or the official RemixOS [video-guide for Windows users](https://www.youtube.com/watch?v=At7_g9ZXu8s).

## BlissRom

Another one useful Open-Source Android ROM for x86.
You can find some additional features preinstalled like Root permission in addition to the Pico version of [OpenGapps](https://github.com/opengapps/).

### Installation

We compiled an updated version of Android 7.1.1 with a more updated kernel useful to use the official WiFi/Bt M.2 module.  

**BlissRom Android 7.1.1**:  
[**bliss_android_x86_64.zip**](http://download.udoo.org/files/UDOO_X86/Android/bliss_android_x86_64.zip)  
sha1: 91635f87f7f900676e255ad7e7e6e7944e81e83c

<span class="label label-warning">Heads up!</span> This is not developed by the UDOO Team so it is not official and supported directly.

Alternatively you can download the builds in the official [download page](http://blissroms.com/downloads/devices.html).

To prepare a bootable USB with the installer you can follow the UDOO [Getting Started](https://www.udoo.org/get-started-x86/) guide, or the official [blissrom documentation](http://blissroms.com/downloads/bliss-x86-install-instructions).

<span class="label label-warning">Heads up!</span> We have noticed some issues during the installation so we suggest to choose the `Legacy` mode at boot.

<span class="label label-warning">Heads up!</span> If after a complete installation Android-x86 doesn't boot properly, we suggest to prepare the partition where you want to install the OS formatting it in `ext4` and **do not** format again the partition during the Android-x86 wizard installation. This is a known issue, we found this solution in different articles, like [this one](https://techposts.org/install-android-6-marshmallow-laptop-pc/), for example.
