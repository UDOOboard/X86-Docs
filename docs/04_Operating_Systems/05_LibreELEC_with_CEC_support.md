**LibreELEC** is a 'Just enough OS' Linux distribution for running Kodi.  
It is efficient with a tiny disk and memory footprint and provides cutting-edge hardware support to deliver a set-top box Kodi experience.

*Kodi* is a free and open-source media player software application developed by the XBMC Foundation.  

LibreELEC is the best choice if you want to build your own set-top box device to connect to your TV.

In this page we release a LibreELEC image that include the [CEC](!Hardware_&_Accessories/CEC-HDMI) and [IR](!Hardware_&_Accessories/Consumer_IR) support for the UDOO X86 to exploit all the functionalities of the board as an HTPC.  

<span class="label label-warning">Heads up!</span> At least the version *1.06* of the UEFI/BIOS firmware of the UDOO X86 need to be installed to make the CEC and IR work properly. Visit the [UEFI Update](!Advanced_Topics/UEFI_update) section to know how to update your board.  
<span class="label label-warning">Heads up!</span> Enable IR functionality from the Setup Utility Menu of the [UEFI/BIOS Firmware](!Hardware_Reference/UEFI_Firmware)

The functionality is provided by a patched version of LibCEC. The Remote Control input activation is automatic and should work out-of-the-box.

## Download the image

### Stable Version
Download the image here: [LibreELEC with CEC support][imagestab]   
SHA256-SUM: `cdd043591153436acb070a9649fdde8a53cd2eb906a0c25efe52448dcdf79e8f`  
Last Commit: `161b7d7942392d8d4dc0a9503d35d13b4be1c303`

This version of LibreELEC is the 9.1 with Linux kernel 5.1.16 (branch *libreelec-9.2*).

### Unstable Version
Download the image here: [LibreELEC with CEC support][imageunstab]   
SHA256-SUM: `62fa5f67b0c483ebe93a80e376f2c09e78b4518df2bcba52a02f4ad9ce0a0cf2`  
Last Commit: `67a5bc8ff369b0aaabcc61b5e4bbb3bfc2ac2a8c`

This version of LibreELEC is the 9.80 with Linux kernel 5.1.15 (branch *master*).


### Old Version
Download the image here: [LibreELEC with CEC support][imageold]   
SHA256-SUM: `6c06708a0b4b28ddaa8a1f918c25cc1defe8d9a6317d2e6859f9eb7a8850bc4e`

This version of LibreELEC is the 9.0 with Linux kernel 4.19 RC8.

## Compile

To compile the image yourself, you just need to enable the *CEC Framework* and
add the `SECO_CEC` support in the Kernel config.

In order to do so, clone the forked repo using the following command.

	git clone https://github.com/ektor5/LibreELEC.tv

It has already the edits you need for enabling the CEC.

Then follow the official guide to compile the image [here](https://libreelec.wiki/compile).

## Flash

Once you have downloaded the image you need to create a bootable USB media.  
In the [Getting Started](https://www.udoo.org/get-started-x86/) section you can find a guide of how to install a Linux distro, the example is based on the Ubuntu OS.

If you are an expert user and you want to do it in a fast way you can *dd* the image on a USB pendrive with the following command, substituting the correct image name and "sdd" with the correct device name:

    zcat "path/of/the/image.gz" | dd of=/dev/sdd bs=4M status=progress

Remove the USB pen when the process has finished.

## Installation

Insert the USB pen and power up the board.
Press ESC to enter the EFI menu and select Boot Manager, then select the USB pen.

When booting you'll be standing in front of a terminal, type `installer` and Enter to install LibreELEC, otherwise type `live` and Enter for a Live session.

Go through the installation wizard to install it permanently into the eMMC or another external drive.

Enjoy the fast boot of LibreELEC.

[imageold]: https://sourceforge.net/projects/udooboard/files/UDOO_X86/LibreELEC/LibreELEC-Generic.x86_64-9.0-devel-20181022184922-461ea72.img.gz/download
[imageunstab]: https://sourceforge.net/projects/udooboard/files/UDOO_X86/LibreELEC/LibreELEC-Generic.x86_64-9.80-devel-20190710181224-ef834cb.img.gz/download
[imagestab]: https://sourceforge.net/projects/udooboard/files/UDOO_X86/LibreELEC/LibreELEC-Generic.x86_64-9.1-devel-20190711122949-7c00387.img.gz/download
