## Introduction

[**UDOO BRICKS**](https://www.udoo.org/udoo-bricks/) are modules you can use to augment your UDOO BOARDS and make them more versatile. Attach them into *I2C Bricks snap-in connector* with the related cable. UDOO BRICKS work along a cascade configuration, so you can attach them all together without wasting space in a truly intuitive way. Thanks to such configuration you can use cables up to 3,5 m long to connect UDOO BRICKS one another.

In the **UDOO X86** the *I2C Bricks snap-in connector(CN24)* is connected to the Intel&reg; Curie&trade; Processor (Arduino 101-compatible side).

<span class="label label-warning">Heads up!</span> The main Intel&reg; Braswell processor cannot access the I2C Brick snap-in bus connector. To work in Linux, Windows or Android with the data from the UDOO BRICKS, you need to pass the data via the [internal serial communication](!/Serial_Libraries/index).

You can use the Bricks modules exactly like I2C modules connected to the I2C bus of the Arduino 101 in *SCL/SDA* Pins.  
**I2C** Bus support more devices simultaneously connected, so you can connect more than one brick to the the *I2C Bricks snap-in connector(CN24)* and connect other modules to the *SCL/SDA* Pins at the same time.

## Light Brick - TSL2561T

The LIGHT BRICK is a light sensor. It’s based on the `TSL2561T` sensor.

You can find documentation as datasheet, schematics, and montage plane in the [Other Resurces](https://www.udoo.org/other-resources/) page of our website, in the `Accessories` tab.

### Usage

To use this sensor and calculate Lux, there's a lot of very hairy and unpleasant math, but you can simply use one of the compatible libraries available in the [`Library Manager`](https://www.arduino.cc/en/guide/libraries) of the Arduino IDE.  
 Open the IDE and click to the *Sketch* menu and then *Include Library > Manage Libraries*.

 In the *Filter your search* edit text type `TSL2561`. You can find these libraries available, all of them properly working:
 * **Adafruit TSL2561** (to use the Adafruit TSL2561 library you need to also install the [Adafruit Sensor](https://github.com/adafruit/Adafruit_Sensor/archive/master.zip) library from the .Zip file)
 * **SparkFun TSL2561**
 * **TSL2561 Arduino Library**

You can use the Example Sketch of each library to read Lux.   
The Brick Light Sensor **I2C Address** is set to `0x29`, you need to modify the Arduino sketch accordingly to this info. Usually the address `0x29` is defined as `TSL2561_ADDR_0` of `TSL2561_ADDR_LOW`.
