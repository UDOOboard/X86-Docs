**LibreELEC** is a 'Just enough OS' Linux distribution for running Kodi.  
It is efficient with a tiny disk and memory footprint and provides cutting-edge hardware support to deliver a set-top box Kodi experience.

*Kodi* is a free and open-source media player software application developed by the XBMC Foundation.  

LibreELEC is the best choice if you want to build your own set-top box device to connect to your TV.

In this page we release a LibreELEC image that include the [CEC](!Hardware_&_Accessories/CEC-HDMI) and [IR](!Hardware_&_Accessories/Consumer_IR) support for the UDOO X86 to exploit all the functionalities of the board as an HTPC.  
This version of LibreELEC is the 9.0 with Linux kernel 4.19 RC8.

<span class="label label-warning">Heads up!</span> At least the version *1.04* of the UEFI/BIOS firmware of the UDOO X86 need to be installed to make the CEC and IRwork properly. Visit the [UEFI Update](!Advanced_Topics/UEFI_update) section to know how to update your board.
<span class="label label-warning">Heads up!</span> Enable IR functionality from the Setup Utility Menu of the [UEFI/BIOS Firmware](!Hardware_Reference/UEFI_Firmware)

The CEC and IR driver for the UDOO X86 will be integrated into the future mainline Linux Kernel so there won't be needed to download a dedicated version to have these functionalities.

## Donwload the image

Donwload the image here: [LibreELEC with CEC support](http://download.udoo.org/files/UDOO_X86/LibreELEC/LibreELEC-Generic.x86_64-9.0-devel-20181022184922-461ea72.img.gz)  
SHA256-SUM: `6c06708a0b4b28ddaa8a1f918c25cc1defe8d9a6317d2e6859f9eb7a8850bc4e`

Once you have downloaded the image you need to create a bootable USB media.  
In the [Getting Started](https://www.udoo.org/get-started-x86/) section you can find a guide of how to install a Linux distro, the example is based on the Ubuntu OS.

If you are an expert user and you want to do it in a fast way you can *dd* the image on a USB pendrive with the following command "Substitute "sdd" with the correct device name":

    zcat LibreELEC-Generic.x86_64-9.0-devel-20181022184922-461ea72.img.gz | dd of=/dev/sdd bs=4M status=progress

Remove the USB pen when the process has finished.

## Installation

Insert the USB pen and power up the board.
Press ESC to enter the EFI menu and select Boot Manager, then select the USB pen.

When booting you'll be standing in front of a terminal, type `installer` and Enter to install LibreELEC, otherwise type `live` and Enter for a Live session.

Go through the installation wizard to install it permanently into the eMMC or another external drive.

Enjoy the really fast boot of LibreELEC.
