UDOO X86 is supplied with an [InsydeH2O®](https://www.insyde.com/products) UEFI BIOS.

It is possible to access to InsydeH2O® Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

## UEFI Update utility

At the following link you can find the latest UEFI Firmware and the UEFI Update Utility to quickly and easily updates flash devices with new UEFI Setup firmware.

[UEFI BIOS + and Update Utility](http://download.udoo.org/files/UDOO_X86/UEFI_update/UDOOX86_B02-UEFI_Update_rel106.zip)

The package contains:
* Latest UEFI Firmware binary
  * Firmware name: 0B020000.106
  * BIOS version:  1.06
  * Release Date:  2019-01-07
  * SHA1 .zip file:  D017F97E014351DA3705E9A8360B1C59E6F5D535
* Update Utility Tool
  * DOS BIOS programming utility
  * Windows 32-bit BIOS programmer
  * Windows 64-bit BIOS programmer
  * Linux 32-bit programmer
  * Linux 64-bit programmer
* Update procedure documentation (.pdf)

Follow the procedure in the .pdf file to update the UEFI BIOS firmware using DOS, Linux or Windows running on your UDOO X86.

<span class="label label-warning">Heads up!</span> Remember that update the UEFI firmware will revert the saved configuration to Factory Default.

Please be aware that using **Windows** programmer, it must be run in a Prompt CMD shell with Administrator privileges.

Using **Linux** programmer, *gcc compiler* and *Kernel-headers* are needed and every operation must be done with root/administrator privileges.  
Linux versions used for the test:
* Ubuntu 16.04 - 16.10 - 17.04 - 18.04
* Debian 8.5
* Fedora 24
* Opensuse 42
