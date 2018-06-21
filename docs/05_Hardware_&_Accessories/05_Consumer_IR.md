## Introduction

Quoting from the Wikipedia page of the [Consumer IR](https://en.wikipedia.org/wiki/Consumer_IR):

> Consumer IR, consumer infrared, or CIR, refers to a wide variety of devices
> employing the infrared electromagnetic spectrum for wireless communications.
> Most commonly found in television remote controls, infrared ports are equally
> ubiquitous in consumer electronics, such as PDAs, laptops, and computers. The
> functionality of CIR is as broad as the consumer electronics that carry it. 

The IR receiver mounted on the board is controlled by the Embedded Controller
(STM32) and it can receive and decode only [RC-5 protocol][rc5] signals.

In this way it is possible to control your UDOO X86 with a simple remote control.

[rc5]: https://en.wikipedia.org/wiki/RC-5

## Use

The driver is developed only for Linux, and it is implemented inside the
[CEC-HDMI driver](CEC-HDMI). Refer to the guide for installation.

<span class="label label-warning">Heads up!</span> Make sure you have installed
an updated FW version (*>= 1.04*) on your UDOO X86.

When it is loaded, it will spawn an *Remote Control* Input device and it can be
managed with the RC Framework and tools such as `ir-keytable`.  
Due to the lack of standardization in the *Consumer IR* remote controls, it
will likely not be configured properly for your remote control.  The procedure
for configuration is the same as the [CEC-HDMI RC Passthrough
device](CEC-HDMI#page_Edit-keymaps)

[Here][rcframework] is a fantastic guide from *YaVDR* about using `ir-keytable`
and how configuring your RC device.

[rcframework]: http://www.yavdr.org/documentation/0.5/en/ch03s03.html#ir-keytable

