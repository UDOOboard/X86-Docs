The UDOO X86 contains an embedded Intel Arduino 101, powered by Intel's [Curie&trade;](http://www.intel.com/content/www/us/en/wearables/wearable-soc.html) module comprising of two cores operating simultaneously.
* The **Intel&reg; Quark SE&trade;** Core, a 32 MHz x86 processor, compatible with the Pentium x86 instruction set. Manages the USB interface (routed internally on the UDOO X86), and Bluetooth Low Energy. Contains 384 kB of on-die flash & 80 kB of on-die SRAM.
* The **ARC**, a 32 MHz Argonaut RISC Core. This is where compiled Arduino Sketches are executed. The ARC can communicate directly with the six-axis accelerometer/gyroscope. The memory subsystem is shared with the Quark SE&trade;, which also manages the communication between the two cores.

### Integrated device references
* [Intel&reg; Curie&trade;](https://software.intel.com/en-us/iot/hardware/curie)
* [Bosch BMI160 six-axis sensor](https://www.bosch-sensortec.com/bst/products/all_products/bmi160)
* [nRF51822 Bluetooth Low Energy chip](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF51822)
