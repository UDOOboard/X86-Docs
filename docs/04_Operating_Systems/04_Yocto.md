## What is Yocto
The Yocto Project is a Linux Foundation workgroup whose goal is to produce tools and processes that will enable the creation of Linux
distributions for embedded software that are independent of the underlying architecture of the embedded software itself.
The project was announced by the Linux Foundation in 2010.
In March 2011, the project aligned itself with OpenEmbedded, an existing framework with similar goals, with the result being The OpenEmbedded-Core Project.
The Yocto Project is an open source project whose focus is on improving the software development process for embedded Linux distributions.
The Yocto Project provides interoperable tools, metadata, and processes that enable the rapid, repeatable development of Linux-based embedded systems.

## Project Scope
The Yocto Project has the aim and objective of attempting to improve the lives of developers of customised Linux systems supporting the ARM, MIPS, PowerPC and x86/x86 64 architectures. A key part of this is an open source build system, based around the OpenEmbedded architecture, that enables developers to create their own Linux distribution specific to their environment.
This reference implementation of OpenEmbedded is called Poky.
There are several other sub-projects under the project umbrella which include EGLIBC, pseudo, cross-prelink, Eclipse integration, ADT/SDK, the matchbox suite of applications, and many others. One of the central goals of the project is interoperability among these tools.
The project offers different sized targets from "tiny" to fully featured images which are configurable and customizable by the end user. The project encourages interaction with upstream projects and has contributed heavily to OpenEmbedded-Core and BitBake as well as to numerous upstream projects, including the Linux kernel.[citation needed] The resulting images are typically useful in systems where embedded Linux would be used, these being single-use focused systems or systems without the usual screens/input devices associated with desktop Linux systems.
As well as building Linux systems, there is also an ability to generate a toolchain for cross compilation and a software development kit (SDK) tailored to their own distribution, also referred to as the Application Developer Toolkit (ADT). The project tries to be software and vendor agnostic. Thus, for example, it is possible to select which package manager format to use (deb, rpm, or ipk).
Within builds, there are options for various build-time sanity/regression tests, and also the option to boot and test certain images under QEMU to validate the build.

## UDOO X86 Yocto image
Download: [core-image-sato-seco-64-udoo-logo.iso.bz2](http://download.udoo.org/files/UDOO_X86/Yocto_braswell/core-image-sato-seco-64-udoo-logo.iso.bz2)     
SHA1: 47b370600a7b1e6f45c0f19bbd93bd29091a1ccb

### Installation
To install Yocto on the eMMC of the UDOO X86 follow this steps:

<span class="label label-warning">Heads up!</span> In order not to risk to flash other drives we suggest to disconnect other storage devices connected.

1. Download the image above on you PC
2. Extract the iso from the .bz2 file using this command from the directory when you downloaded the file:  

        bzip2 -d core-image-sato-seco-64-udoo-logo.iso.bz2
Note, that this command will not preserve original archive file.  
To preserve the original archive, add the `-k` option:

        bzip2 -dk core-image-sato-seco-64-udoo-logo.iso.bz2

3. Create a bootable USB installation drive as for the other Linux distributions following the guide [Getting Started](https://www.udoo.org/get-started-x86/)
4. If the eMMC device is properly detected, the installation will ask if you want to install the image there, type `Y` and press `Enter`.
5. Choose the percentage of swap on total drive size. You can type `0` and press `Enter`
5. The installation should take about a minute.

<span class="label label-warning">Heads up!</span> If you want the fastest boot as possible, once the installation is complete we suggest to modify the file `grub.cfg` changing the `timeout` voice to `0` (10 seconds are set by default).

## Build From Source

At the link below you can find the source used to compile this image, it is forked from the standard Yocto released by Intel&reg; for the **Bay Trail** family processors.

Download: [meta-seco.7z](http://download.udoo.org/files/UDOO_X86/Yocto_braswell/meta-seco.7z)
SHA1: 90128847699C2EC7B3729F61E0B3D9EF9167EA5F

Inside the package you can find a guide you can follow to compile the Yocto image.
