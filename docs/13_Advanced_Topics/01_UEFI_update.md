UDOO X86 is supplied with an [InsydeH2O®](https://www.insyde.com/products) UEFI BIOS.

It is possible to access to InsydeH2O® Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

## UEFI Update utility

At the following link you can find the latest UEFI Firmware and the UEFI Update Utility to quickly and easily updates flash devices with new UEFI Setup firmware.

[UEFI BIOS Update Utility](http://download.udoo.org/files/UDOO_X86/UEFI_update/UDOOX86_B02-UEFI_Update_rel102.zip)

The package contains:
* Latest UEFI Firmware binary
  * Firmware name:       0B020000.102
  * BIOS version:        1.02
  * Release Date:        04/21/2017
  * Firmware version:    0F08
  * Bootloader version:  0B00
  * SHA1: a9ff5b5f019b167281363cd9300e4b6f9686757e
* Update Utility Tool
  * DOS BIOS programming utility
  * Windows 32-bit BIOS programmer
  * Windows 64-bit BIOS programmer
  * Linux 32-bit programmer
  * Linux 64-bit programmer
* Update procedure documentation (.pdf)

Follow the procedure in the .pdf file to update the UEFI BIOS firmware using DOS, Linux or Windows running on your UDOO X86.

<span class="label label-warning">Heads up!</span> Remember that update the UEFI firmware will revert the saved configuration to Factory Default.

Please be aware that using **Windows** programmer, it must be run in a cmd shell with Admin privileges.

Using **Linux** programmer, *gcc compiler* and *Kernel-headers* are needed and every operation must be done with root/administrator privileges.  
Linux versions used for the test:
* Ubuntu 16.04, 16.10
* Debian 8.5
* Fedora 24
* Opensuse 42
