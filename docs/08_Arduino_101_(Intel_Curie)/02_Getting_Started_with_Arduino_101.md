
To start programming the Arduino 101 (Intel&reg; Curie&trade;) embedded microcontroller of the UDOO X86 you need the `Arduino IDE` or the `Arduino Web IDE`.

You can refer the [Getting Started with the Arduino/Genuino 101](https://www.arduino.cc/en/Guide/Arduino101) page of the Arduino website.  
This Arduino page will guide you through the [installation of the IDE and the core board manager of the Arduino 101](https://www.arduino.cc/en/guide/arduino101#toc2) other than everything you need to program the Arduino and use the pinout.

## Linux known issues

#### Installation

In some previous Arduino IDE version there was some installation issues, but now you can download the latest Arduino IDE version **(at least Arduino IDE 1.8.3)** and you should not find any Linux installation.

#### Upload Procedure

Some `Linux` distributions need to be configured to to gain upload permissions.  
Inside the Arduino 101 core you can find a script to allow the user to use the serial device. Using the latest Arduino 101 core package v2.0.2 run the script with this commands:

    chmod +x ~/.arduino15/packages/Intel/hardware/arc32/2.0.2/scripts/create_dfu_udev_rule
    sudo ~/.arduino15/packages/Intel/hardware/arc32/2.0.2/scripts/create_dfu_udev_rule

## USB Devices

The USB device where you can find the Arduino 101 (Intel&reg; Curie&trade;) embedded may vary in accordance with the number of USB devices connected to the board.  
Usually, you should find the Arduino 101 in the `COM3` in **Windows 10** and `/dev/ttyACM0` in **Unix/Linux** OS.

Check the Arduino page also for [Tutorial](https://www.arduino.cc/en/guide/arduino101#toc8), [Curie&trade; Libraries](https://www.arduino.cc/en/guide/arduino101#toc9) ad other useful information.
