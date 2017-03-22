The **GPIO** (*General-Purpose Input/Output*) peripheral provides dedicated general-purpose pins that can be configured as either inputs or outputs.
When configured as an output, it is possible to write to an internal register to control the state driven on the output pin. When configured as an input, it is possible to detect the state of the input by reading the state of an internal register. In addition, the GPIO peripheral can produce CORE interrupts.

**UDOO X86** features a total of **36** GPIOs available on the external Pinout connectors.

* **16** GPIOs are available in the external Pinout columns manageable from the main Intel&reg; Braswell processor of the UDOO X86. These Pins are *1.8V only compliant*.
* **20** GPIOs are available in the internal Arduino Pinout columns manageable from the Intel&reg; Curie&trade; processor of the Arduino 101 embedded. These Pins are *3.3V compliant and 5V tollerant*.

# Braswell GPIOs

In the following image you can see in grey labels the 16 GPIOs manageable from the main Intel&reg; Braswell.

<a href="../img/x86_pinout_braswell.png" target="_blank"><img style="width:600px; " src="../img/x86_pinout_braswell.png"></a>

Visit the [Pinout Braswell](!Hardware_Reference/Pinout_Braswell) section to see how to **enable/disable** the GPIO function for these pins from the UEFI BIOS Setup of the UDOO X86.

The GPIO function is enabled by default in the UEFI BIOS Setup configuration of the UDOO X86.

## Linux Manipolation

The Linux driver used to manage the UDOO X86 Braswell GPIOs is [Cherryview/Braswell pinctrl driver](https://github.com/torvalds/linux/blob/master/drivers/pinctrl/intel/pinctrl-cherryview.c)

In the following tables you can find GPIO numbers assigned by the driver to each Pin that can act as GPIO.

**PinHeader Connector CN13**

| Physical Pin Number | GPIO NUMBER | GPIO device name from the Linux Driver |
|---------------------|-------------|----------------------------------------|
| **24**              |     346     | /sys/class/gpio/gpio346                |
| **25**              |     351     | /sys/class/gpio/gpio351                |
| **26**              |     344     | /sys/class/gpio/gpio344                |
| **27**              |     349     | /sys/class/gpio/gpio349                |
| **28**              |     347     | /sys/class/gpio/gpio347                |
| **29**              |     350     | /sys/class/gpio/gpio350                |
| **30**              |     366     | /sys/class/gpio/gpio366                |

**PinHeader Connector CN14**

| Physical Pin Number | GPIO NUMBER | GPIO device name from the Linux Driver |
|---------------------|-------------|----------------------------------------|
| **36**              |     497     | /sys/class/gpio/gpio497                |
| **37**              |     499     | /sys/class/gpio/gpio499                |

**PinHeader Connector CN12**

| Physical Pin Number | GPIO NUMBER | GPIO device name from the Linux Driver |
|---------------------|-------------|----------------------------------------|
| **40**              |     408     | /sys/class/gpio/gpio408                |
| **41**              |     326     | /sys/class/gpio/gpio326                |
| **42**              |     332     | /sys/class/gpio/gpio332                |
| **43**              |     329     | /sys/class/gpio/gpio329                |
| **44**              |     336     | /sys/class/gpio/gpio336                |
| **45**              |     333     | /sys/class/gpio/gpio333                |
| **46**              |     330     | /sys/class/gpio/gpio330                |

Here you can find the Driver Documentation in the kernel that explain the use of the [sysfs inferface](https://www.kernel.org/doc/Documentation/gpio/sysfs.txt).

#### Export GPIOs

In `/sys/class/gpio` folder there are two files that allow you to *export* pins for access and *unexport* pins to remove access.
```bash
/sys/class/gpio/export
/sys/class/gpio/unexport
```
To export a GPIO so that we can read, write and control the pin, we simply write the GPIO_NUMBER to the export file:
```bash
echo GPIO_NUMBER > /sys/class/gpio/export
```
For example, to export `GPIO 350`:
```bash
echo 350 > /sys/class/gpio/export
```
Once GPIO pin 350 is exported the following files (or links to files) are created in a new directory, **gpio350**.
```bash
/sys/class/gpio/gpio350/direction
/sys/class/gpio/gpio350/value
```
A GPIO can be set in *input* or *output* configuration.  
In *input* means you can read the value of the voltage connected to the pins.  
In *output* means you can forces a pin to take a specific voltage.

It is possible to switch a GPIO in *input* or *output* mode by writing either `in` or `out` to the direction file:
```bash
# set gpio 350 to input
echo in > /sys/class/gpio/gpio350/direction

# set gpio 350 to output
echo out > /sys/class/gpio/gpio350/direction
```
To verify the voltage direction, just read the same file:
```bash
cat /sys/class/gpio/gpio350/direction
```
#### Write values
To write a low or high value on a GPIO, you need to write `0` or `1` in the *value* file:
```bash
# set gpio 350 to low value - 0 volts
echo 0 > /sys/class/gpio/gpio350/value

# set gpio 350 to high value - 1.8 volts
echo 1 > /sys/class/gpio/gpio350/value
```
In order to set the value, the GPIO must be in the `out` direction.

#### Read values
If the direction is set to `in`, it is possible to read the GPIO value reading the same *value*  file:
```bash
cat /sys/class/gpio/gpio350/value
```
If the direction is set to `out` and you try to read the value, is not guaranteed that the value is coherent with the voltage found on the external pinout.
