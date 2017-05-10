## UDOO X86 Serial Libraries Examples

Serial Libraries Communication Samples for [UDOO Board](https://www.udoo.org)

These example’s scripts are meant to demonstrate how to implement a uni\bidirectional communication between an Arduino sketch (running on the Arduino&trade; 101 Intel&reg; Curie&trade; embedded) and a binary application on the Braswell processor running Linux.

The Arduino sketch will remain the same no matter which programming language you’ll use to develop the binary on Linux.

<span class="label label-warning">Heads up!</span> The sources could be used also for Windows programs, however the libraries installation and compilation instructions aren't valid.

There are two example scripts for each programming language: C, Java, PHP, Python.

You can find the whole repo in our [Github Channel](https://github.com/UDOOboard/serial_libraries_examples).
Clone the repo in your system and switch to proper `udoo-x86` branch using these commands on a terminal:

    git clone https://github.com/UDOOboard/serial_libraries_examples.git
    cd serial_libraries_examples
    git checkout udoo-x86

<span class="label label-warning">Heads up!</span> Make sure the user has the proper permission to read and write from the Arduino&trade; 101 serial device (`/dev/ttyACM0` by default)

Each program is meant to be executed while the matching Arduino Sketch is running on Arduino&trade; 101 Intel&reg; Curie&trade;.

Program the Arduino&trade; embedded with the sketch named `arduino_serial_example.ino` before run these examples:

    c_serial_example.c
    java_serial_example.java
    php_serial_example.php
    python_serial_example.py


Program the Arduino&trade; embedded with the sketch named `arduino_serial_example_bidirectional.ino` before run these examples:

    c_serial_example_bidirectional.c
    java_serial_example_bidirectional.java
    php_serial_example_bidirectional.php
    python_serial_example_bidirectional.py


## Useful libraries to communicate with Arduino from a software on the Braswell processor

### Firmata

The Firmata library implements the [Firmata protocol](https://github.com/firmata/protocol) for communicating with software on the host computer. This allows you to write custom firmware without having to create your own protocol and objects for the programming environment that you are using.

You can check the Firmata documentation in the [Arduino Reference page](https://www.arduino.cc/en/Reference/Firmata) or the [firmata wiki page](http://firmata.org/wiki/Main_Page).  
Here you find the [Firmata firmware for Arduino](https://github.com/firmata/arduino).  
You can install the Firmata library directly from the Arduino IDE library manager.
