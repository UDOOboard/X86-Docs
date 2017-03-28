The Arduino 101 side (Intel® Curie™) of the UDOO X86 can take care of the Braswell power management.  
It can act as the Power Button(PWR) of the board connected directly to the Braswell processor. This means that an Arduino 101 sketch, that it's always running while the board is powered up, can for example turn on/off the Braswell main processor or wake the OS from the suspend state.

The Arduino 101 on board can wake up the Braswell processor depending on various triggers. For example, it can wake up the Braswell prcessor if the temperature, registered by a connected temperature sensor, increases over a certain threshold. Other examples of triggers may be a BLE signal or a movement tracked by the 6-axis motion sensor on board, defining features of Arduino 101. By exploiting the Arduino capabilities, you can set up the trigger you want to get the behaviour you expect from the system.

The Arduino 101 (Intel® Curie™) can trigger a power signal of the Braswell processor by producing a **20ms low pulse** in the **Arduino Pin 9** (IO9/PWM3 signal in the schematics). Technically speaking the pulse is catched by a SMT32 microcontroller onboard(STM32F100R4H6) and propagated to the Braswell to wake it up.

You need to enable this feature of the UDOO X86 board in the UEFI setup(SCU). You can find the **Curie Power Management** option in the menu **Power**:

    Power

    ...
    Curie Power Management    <Enabled>
    Power On Intel Curie      <Enabled>


The option you can choose for the **Curie Power Management** are:

    <Disabled>    =   Intel Curie will never change the power status of the system

    <Wake Only>   =   Intel Curie only be able to wake the system from S3/S4/S5

    <Enabled>     =   Intel Curie will be able to put the system in a lower power
                      state(S3/S4/S5 depending on OS configuration) and wake it

## Example

Following an example of an Arduino sketch that could be used to trigger a power signal from the Arduino 101 (Intel® Curie™) when a button is pressed:

#### Circuit design

<a href="../img/x86_power_mng_circuit.png" target="_blank"><img style="width:600px; " src="../img/x86_power_mng_circuit.png"></a>

#### Arduino sketch

```
int reset_pin = 9;    /* Triggers the power signal */
int input_pin = 2;    /* Input Button connected. Set in pull down with a resistor */

int pulse_time = 20;
volatile boolean power_pressed = false;

void power_interrupt() {
  /* When the button (connected to the Pin 2) is pressed, the attached interupt runs this routine */
  power_pressed = true;
}

void setup() {
  pinMode(reset_pin, OUTPUT);
  digitalWrite(reset_pin, HIGH);

  pinMode(input_pin, INPUT);
  attachInterrupt(digitalPinToInterrupt(input_pin), power_interrupt, RISING);
}

void loop() {
  if (power_pressed) {
    digitalWrite(reset_pin, LOW);
    delay(pulse_time);    /*  Reset pin goes LOW for 20ms */
    digitalWrite(reset_pin, HIGH);
    power_pressed = false;
  }

  /* Your main code goes in this loop, as before  */
  delay(10);
}
```
