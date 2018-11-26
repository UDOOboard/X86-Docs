UDOO X86 is a Single Board Computer based on the *N-Series Intel® Pentium® / Celeron® and x5-Series Atom* family of System-on-Chips (SoCs) formerly coded as **Braswell**, a series of Quad Core SoCs with **64-bit instruction set** and very low TDP.

Thanks to the x86_64 instruction set, the **UDOO X86** supports the *Windows* distribution for **32-bit**(aka i386, IA-32, x86-32, x86_32) and **64-bit**(aka x64, x86-64, x86_64).

We suggest to always use a **64-bit** Windows version.

<span class="label label-warning">Heads up!</span> Please notice that total amount of 8GB of RAM of the UDOO X86 ULTRA version would be usable only with 64-bit OS. Total amount of memory available with a 32-bit OS depends on the OS itself (less than 4GB, however).

The supported version of Windows are:
* Microsoft® Windows® 7 (32/64 bit)
* Microsoft® Windows® 8.1 (32/64 bit)
* Microsoft® Windows® 10 (32/64 bit)
* Microsoft® Windows® Embedded Standard 7 /8 (32/64 bit)

In the [Getting Started](https://www.udoo.org/get-started-x86/) section you can find a guide of how to install Windows, the example is based on Windows® 10 64-bit.

The procedure to install a Windows® 7 version is a little different so read the dedicated section on the bottom of this page.

<span class="label label-warning">Heads up!</span> The *Braswell Processors* of the UDOO X86 and the *Wi-Fi/BT Intel® AC3168 module* are released only few time ago so we suggest to use Windows&reg; 10 64-bit to find all the latest drivers already installed and have all the devices operating properly.

<span class="label label-warning">Heads up!</span> If you have issues with the TRRS microphone in Windows® 10 try to install the *Realtek High Definition Audio Codecs* audio drivers from [this page](https://www.realtek.cz/download-ALC283-sound-driver-for-Windows10-64bit.html)

In order to download the latest updated versions of the Intel&reg; devices drivers (e.g. Graphics HD drivers, chipset, wireless networking) we suggest to download and run the [Intel® Driver & Support Assistant](https://downloadcenter.intel.com/download/24345/Intel-Driver-Support-Assistant) for Windows&reg;.

### Windows® 7 Installation

Please be aware that Windows® 7 OS doesn’t have native support for the xHCI controller for **USB 3.0** port. It will be supported only after installing chipset’s driver.  
This could lead to problems during OS installation, since during this phase USB keyboard and mouse will not work, if connected to any of the USB ports available on UDOO x86 board.

It is possible to force the Windows® 7 Support for Keyboard and Mouse on USB ports by entering UEFI Setup utility(SCU) before performing Windows® 7 and chipset’s driver installation.  
You can find the **Win7 Keyboard/Mouse Support** option in the menu **Advanced**, sub menu **Other
Configuration**:

    Advanced

    ...
    Other Configuration

    ...
    Win7 Keyboard/Mouse Support   <Enabled>


<span class="label label-warning">Heads up!</span> Windows 7 does not include any driver support for **eMMC** devices so installation in this storage device is not supported by this OS.
