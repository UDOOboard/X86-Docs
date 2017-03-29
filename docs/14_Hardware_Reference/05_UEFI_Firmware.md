## UEFI Firmware

Basic setup of the board can be done using *[InsydeH2O®](https://www.insyde.com/products) Setup Utility*.

It is possible to access to InsydeH2O Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase. The UEFI Menu show the following options:

<a href="../img/uefi_menu.BMP" target="_blank"><img style="width:400px; " src="../img/uefi_menu.BMP"></a>

* **Continue**: The Boot continue with the configured boot option.
* **Boot Manager**: Here you can choose the device to boot from – eMMC, Micro SD, SATA drive, USBdisk, LAN, or other supported boot device.

<a href="../img/uefi_bootmanager.BMP" target="_blank"><img style="width:400px; " src="../img/uefi_bootmanager.BMP"></a>

* **Device Manager**:
* **Boot From File**:
* **Secure Boot Option**:
* **SCU**: The *System Configuration Utility* is where you can configure basic system settings like the date and time, to advanced features like the security configuration. You can also set your preferred power options, for example, making sure the computer turns back on after a loss of power, useful if the board is located remotely.  

<div class="alert alert-danger" role="alert">
  <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
  <span class="sr-only">Warning!</span>
  Warning: Please do NOT "play" with the SCU menu voices if you don't know what you are doing. For example, if you disable USB ports or Video Outputs you will not be able to interact with the SCU to revert this situation.
</div>


<a href="../img/uefi_scu.BMP" target="_blank"><img style="width:400px; " src="../img/uefi_scu.BMP"></a>  

## UDOO X86 Hardware and UEFI BIOS User Manual

For a complete explanation of SCU menu items you can download the exhaustive UDOO X86 Hardware and UEFI User Manual *(link coming soon)* <TODO: fix link>
