UDOO X86 is supplied with an [InsydeH2O®](https://www.insyde.com/products) UEFI Firmware, you can use it to setup of the board.

If you are looking for how to update UEFI Firmware go to the [UEFI update](!/Advanced_Topics/UEFI_update) section.

It is possible to access to InsydeH2O® Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

<span class="label label-warning">Heads up!</span> Some wireless or mechanical keyboards that doesn't respect the standard USB HID protocol could doesn't work in the UEFI BIOS Firmware menu. Regarding the wireless keyboards we tested these that are proper working also in the UEFI BIOS menu: [Logitech k400r](http://www.logitech.com/en-us/product/wireless-touch-keyboard-k400r), [Logitech k400 plus](http://www.logitech.com/product/wireless-touch-keyboard-k400-plus), [Microsoft All-in-One Media Keyboard](https://www.microsoft.com/accessories/products/keyboards/all-in-one-media-keyboard/n9z-00013).

<div class="alert alert-danger" role="alert">
  <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
  <span class="sr-only">Warning!</span>
  Warning: Please do NOT "play" with the SCU menu choices if you don't know what you are doing. For example, if you disable USB ports or Video Outputs you will not be able to interact with the SCU to revert this condition. If you stumbling upon this case take a look at the **Restore Factory configuration** section below.
</div>

## UDOO X86 Hardware and UEFI BIOS User Manual

For a complete explanation of the System Configuration Utility menu items you can download the exhaustive [UDOO X86 Hardware and UEFI BIOS User Manual](http://download.udoo.org/files/UDOO_X86/Doc/UDOO_X86_MANUAL.pdf)

## Setup Utility Menu

The UEFI Firmware Setup Utility Menu show the following options:

<span class="label label-warning">Heads up!</span> Since some resolutions or monitors are not managed well by the firmware, if you get a black screen when you try to enter in one of the UEFI Firmware Setup Utility Menu options, try using another Display with a 1080 resolution (HDMI or DisplayPort) or a different cable.

<a href="../img/uefi_menu.png" target="_blank"><img style="width:400px; " src="../img/uefi_menu.png"></a>

* **Continue**: The Boot continue with the configured boot option.
* **Boot Manager**: Here you can choose the device to boot from – eMMC, Micro SD, SATA drive, USBdisk, LAN, or other supported boot device.

<a href="../img/uefi_bootmanager.png" target="_blank"><img style="width:400px; " src="../img/uefi_bootmanager.png"></a>

* **Device Manager**:
* **Boot From File**:
* **Secure Boot Option**:
* **SCU**: The *System Configuration Utility* is where you can configure basic system settings like the date and time, to advanced features like the security configuration. You can also set your preferred power options, for example, making sure the computer turns back on after a loss of power, useful if the board is located remotely.  

<a href="../img/uefi_scu.png" target="_blank"><img style="width:400px; " src="../img/uefi_scu.png"></a>  

## Restore Factory configuration

You can restore the factory default settings from the SCU pressing the **F9** key.

You can also restore the factory UEFI BIOS configuration with a simple procedure involving the RTC battery: when the board is NOT connected to any power source, **unplug the RTC battery** on the bottom side of the board and keep it unplugged for **at least 1 minute**. Plug the RTC battery again and power up the board, all the configurations should now be reverted to the factory defaults.

Updating the UEFI BIOS to a newer version will also restore the new factory default configuration.

<span class="label label-warning">Heads up!</span> You can use the RTC battery procedure starting from the **UEFI BIOS v1.03** so check to have your UDOO X86 [updated](!/Advanced_Topics/UEFI_update).

If you cannot use the precedents methods take a look at this useful [threads of Jetguy](https://www.udoo.org/forum/threads/reset-bios-jumper-or-pins.6674/) in the UDOO Forum.
