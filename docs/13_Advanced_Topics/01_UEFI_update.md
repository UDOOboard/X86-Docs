UDOO X86 is supplied with an [InsydeH2O®](https://www.insyde.com/products) UEFI BIOS.

It is possible to access to InsydeH2O® Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

## UEFI Update utility

At the following link you can find the latest UEFI Firmware and the UEFI Update Utility to quickly and easily updates flash devices with new UEFI Setup firmware.

[UEFI BIOS + and Update Utility](http://download.udoo.org/files/UDOO_X86/UEFI_update/UDOOX86_B02-UEFI_Update_rel103.zip)

The package contains:
* Latest UEFI Firmware binary
  * Firmware name:       0B020000.103
  * BIOS version:        1.03
  * Release Date:        06/08/2017
  * SHA1 .zip file: 7494bc2184ff7b57422d2c5610e329d5be591308
* Update Utility Tool
  * DOS BIOS programming utility
  * Windows 32-bit BIOS programmer
  * Windows 64-bit BIOS programmer
  * Linux 32-bit programmer
  * Linux 64-bit programmer
* Update procedure documentation (.pdf)

Follow the procedure in the .pdf file to update the UEFI BIOS firmware using DOS, Linux or Windows running on your UDOO X86.

<span class="label label-warning">Heads up!</span> Remember that update the UEFI firmware will revert the saved configuration to Factory Default.

<span class="label label-warning">Heads up!</span> Note that the description in the menu item **Power -> Curie Power Management** is incorrect and will be updated with the next UEFI BIOS release. The correct sequence to be used to power-on/power-off the Braswell processor is the one described in the page of this documentation [Braswell Power Management from Arduino 101](!/Arduino_101_\(Intel_Curie\)/Braswell_Power_Management_From_Arduino_101).

Please be aware that using **Windows** programmer, it must be run in a cmd shell with Administrator privileges.

Using **Linux** programmer, *gcc compiler* and *Kernel-headers* are needed and every operation must be done with root/administrator privileges.  
Linux versions used for the test:
* Ubuntu 16.04 - 16.10 - 17.04
* Debian 8.5
* Fedora 24
* Opensuse 42
