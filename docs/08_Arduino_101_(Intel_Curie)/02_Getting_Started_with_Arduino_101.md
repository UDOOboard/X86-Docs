
To start programming the Arduino 101 (Intel&reg; Curie&trade;) embedded microcontroller of the UDOO X86 you need the `Arduino IDE` or the `Arduino Web IDE`.

You can refer the [Getting Started with the Arduino/Genuino 101](https://www.arduino.cc/en/Guide/Arduino101) page of the Arduino website.  
This Arduino page will guide you through the [installation of the IDE and the core board manager of the Arduino 101](https://www.arduino.cc/en/guide/arduino101#toc2) other than everything you need to program the Arduino and use the pinout.

## Linux known issues

#### Installation

Unfortunately the **Arduino IDE 1.8.2** was released with a bug in the `install.sh` script to install the software on Linux.  
If you cannot install Arduino IDE 1.8.2 you need to edit with a text editor the `install.sh` script in this way:

At the code line *9* Modify the `RESOURCE_NAME` variable from `RESOURCE_NAME=cc.arduino.arduinoide` to `RESOURCE_NAME=arduino-arduinoide` like you can see in [this commit of the Arduino IDE source](https://github.com/arduino/Arduino/pull/6110/commits/92fd7232da8b3c511c29e587929b453f6fb697b1).  
This fix is already merged in the Arduino source and will be available on the next  Arduino IDE 1.8.3 release.

#### Upload Procedure

Some Linux distributions need to be configured to to gain upload permissions.  
Inside the Arduino 101 core you can find a script to allow the user to use the serial device. Using the latest Arduino 101 core package v2.0.2 run the script with this command:

    sudo ~/.arduino15/packages/Intel/tools/arduino101load/1.6.4+1.18/scripts/create_dfu_udev_

## USB Devices

The USB device where you can find the Arduino 101 (Intel&reg; Curie&trade;) embedded may vary in accordance with the number of USB devices connected to the board.  
Usually, you should find the Arduino 101 in the `COM3` in **Windows 10** and `/dev/ttyACM0` in **Unix/Linux** OS.

Check the Arduino page also for [Tutorial](https://www.arduino.cc/en/guide/arduino101#toc8), [Curie&trade; Libraries](https://www.arduino.cc/en/guide/arduino101#toc9) ad other useful information.
