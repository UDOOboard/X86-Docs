The UDOO X86 contains an embedded Intel Arduino 101, powered by Intel's [Curie&trade;](http://www.intel.com/content/www/us/en/wearables/wearable-soc.html) module comprising of two cores operating simultaneously.
* The **Intel&reg; Quark SE&trade;** Core, a 32 MHz x86 processor, compatible with the Pentium x86 instruction set. Manages the USB interface (routed internally on the UDOO X86), and Bluetooth Low Energy. Contains 384 kB of on-die flash & 80 kB of on-die SRAM.
* The **ARC**, a 32 MHz Argonaut RISC Core. This is where compiled Arduino Sketches are executed. The ARC can communicate directly with the six-axis accelerometer/gyroscope. The memory subsystem is shared with the Quark SE&trade;, which also manages the communication between the two cores.

### Integrated device references
* [Intel&reg; Curie&trade;](https://software.intel.com/en-us/iot/hardware/curie)
* [Bosch BMI160 six-axis sensor](https://www.bosch-sensortec.com/bst/products/all_products/bmi160)
* [nRF51822 Bluetooth Low Energy chip](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF51822)


## Getting Started with Arduino 101

To start programming the Arduino 101 (Intel&reg; Curie&trade;) embedded microcontroller of the UDOO X86 you need the `Arduino IDE` or the `Arduino Web IDE`.

You can refer the [Getting Started with the Arduino/Genuino 101](https://www.arduino.cc/en/Guide/Arduino101) page of the Arduino website.  
This Arduino page will guide you through the [installation of the IDE and the core board manager of the Arduino 101](https://www.arduino.cc/en/guide/arduino101#toc2) other than everything you need to program the Arduino and use the pinout.

The USB device where you can find the Arduino 101 (Intel&reg; Curie&trade;) embedded may vary in accordance with the number of USB devices connected to the board.  
Usually, you should find the Arduino 101 in the `COM3` in **Windows 10** and `/dev/ttyACM0` in **Unix/Linux** OS.

Check the Arduino page also for [Tutorial](https://www.arduino.cc/en/guide/arduino101#toc8), [Curie&trade; Libraries](https://www.arduino.cc/en/guide/arduino101#toc9) ad other useful information.
