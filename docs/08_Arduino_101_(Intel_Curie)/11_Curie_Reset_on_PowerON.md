Arduino 101 (Intel&reg; Curie&trade;) firmware doesn't manage correctly the USB serial communication during the reboot procedure, or after the suspend state resume of the computer
which is connected to.

Leaving the Arduino 101 connected to the PC (as for an embedded installation or as in the UDOO X86 setup), the Serial
communication over USB (Arduino Serial Object) doesn't work properly at reboot or after suspend state resume.

Both in Windows or Linux the COM or tty is shown at reboot, but it doesn't allow you to write data from PC to Arduino101 throught the Serial.
In this case Arduino IDE freezes while trying to write data on Serial through Serial Monitor.

Only a Master Reset resolves this issue.

## UDOO X86 solution

To resolve this issue the UDOO X86 implements a hardware solution:
The Braswell x86 main processor can internally act on the Master Reset signal of the Intel&reg; Curie&trade;, resetting
both the cores (Quark SE and ARC) in the Curie&trade; SoC and restarting the sketch and the USB communication.

This feature can be Enabled/Disabled by the UEFI BIOS setup (SCU).
You can find the **Curie Reset on PowerON** option in the menu **Power**:

    Power
    ...
      
    Curie Reset on PowerON    <Enabled>

    If enabled the system will automatically reset the Intel Curie when the system
    is waking from a low power state (S3/S4/S5)

By default this feature is enabled until the bug is fixed in the Intel's Arduino 101 firmware.  
This issue [CDCSerial not available after PC reboot or resume from suspend](https://github.com/01org/corelibs-arduino101/issues/399) is opened in the Intel's [corelibs-arduino101](https://github.com/01org/corelibs-arduino101) repository.  
You can `Add your reaction` to thumbs up `👍(+1)` the issue.


### Manage the possible loss of value of the variables

Since this solution implemented in the UDOO X86 acts on the Master Reset signal of the Intel&reg; Curie&trade;, the sketch is reset and restarted at reboot or after the suspend state resume of the Braswell processor. Therefore the sketch isn't erased but you will lose the value of the variables.

To avoid this you can use the Arduino [EEPROM library](https://www.arduino.cc/en/Reference/EEPROM) to permanently save the values of the variables.

The Arduino 101 embedded has an emulated EEPROM space of **1024 bytes**: memory whose values are kept when the board is turned off (like a tiny hard drive).

For example you can simply store and get values using the methods
`EEPROM.put(eeAddress, f);` and `EEPROM.get(eeAddress, f);`

Check the [Arduino EEPROM library](https://www.arduino.cc/en/Reference/EEPROM) page or the [Intel EEPROM Library V2.0](https://github.com/01org/corelibs-arduino101/tree/master/libraries/EEPROM) for exhaustive references and examples.
