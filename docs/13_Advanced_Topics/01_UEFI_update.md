UDOO X86 is supplied with an [InsydeH2O®](https://www.insyde.com/products) UEFI BIOS.

It is possible to access to InsydeH2O® Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

## UEFI Update utility

At the following link you can find the latest UEFI Firmware and the UEFI Update Utility to quickly and easily updates flash devices with new BIOS firmware.

[UEFI BIOS Update Utility](http://download.udoo.org/files/UDOO_X86/UEFI_update/UDOOX86_B02-Bios_Update_rel101.zip)

The package contains:
* Latest UEFI Firmware binary
  * Firmware name:       0B020000.101
  * BIOS version:        1.01
  * Release Date:        02/20/2017
  * Firmware version:    0F08
  * Bootloader version:  0B00
  * SHA1: b573f1534cdfd89b4073b2f1f6a15198d33a092a
* Update Utility Tool
  * DOS BIOS programming utility
  * Windows 32-bit BIOS programmer
  * Windows 64-bit BIOS programmer
  * Linux 32-bit programmer
  * Linux 64-bit programmer
* Update procedure documentation (.pdf)

<span class="label label-warning">Heads up!</span>  It is strongly suggested to reset the CMOS after every update by setting the BIOS to Factory Default.

Please be aware that using **Windows** programmer, it must be run with Admin privileges.

Using **Linux** programmer, *gcc compiler* and *Kernel-headers* are needed and every operation must be done with root/administrator privileges.  
Linux versions used for the test:
* Ubuntu 16.04
* Debian 8.5
* Fedora 24
* Opensuse 42
