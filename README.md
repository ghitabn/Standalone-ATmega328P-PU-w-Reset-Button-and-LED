# Standalone ATmega328P-PU w Reset Button and LED

## 1. Description

This tutorial shows how to setup a standalone ATmega328P-PU microcontroller (breadboard or PCB) in an Arduino compatible mode.
The microcontroller should be pre-loaded with the Arduino bootloader in order to be able to easily upload Arduino sketches using an additional Adruino board. The setup helps to reduce costs and power conpsumtion, in particular for remote devices (i.e. remote sensors).

Difficulty level: intermediate.

## 2. Parts

* 1 x Atmega328P-PU (w Arduino Uno bootloader installed);
* 1 x socket 28 pin standard DIP (narrow);
* 1 x crystal 16 MHz;
* 2 x capacitors 18pF;
* 1 x capacitor 100nF;
* 1 x resistor 680 Ohm;
* 1 x resistor 10 KOhm;
* 1 x reset button;
* 1 x half-size breadboard & wires.

The setup could be done on a custom-built PCB as well (photo below).

Note. The use of a regulated power supply (5V) is highly recommended. In this tutorial the voltage is supplied by a 9V battery through a 5V switching step-up/step-down voltage regulator (S7V7FS).

## 3. Schematics

* ATmega328P-PU to Arduino pin mapping:

![Standalone ATmega328P-PU Arduino pinout!](/res/Standalone_ATmega328P-PU_Arduino_pinout.png "Standalone ATmega328P-PU Arduino pinout")

* Standalone ATmega328P-PU w Reset Button and LED schematics:

![Standalone ATmega328P-PU Arduino schem!](/res/Standalone_ATmega328P-PU_w_Reset_Button_and_LED_schem.jpg "Standalone ATmega328P-PU Arduino schem")

## 4. Assembly (breadboard and PCB)

* breadboard assembly:

![Standalone ATmega328P-PU Arduino bboard!](/res/Standalone_ATmega328P-PU_w_Reset_Button_and_LED_bboard.JPG "Standalone ATmega328P-PU Arduino bboard")

* PCB assembly:

![Standalone ATmega328P-PU Arduino PCB!](/res/Standalone_ATmega328P-PU_w_Reset_Button_and_LED_PCB.JPG "Standalone ATmega328P-PU Arduino PCB")

## 5. Programming

In order to upload an Arduino sketch, several techniques are available with or without additional hardware (please see reference materials). Easiest way is to temporary use an additional Arduino Uno board connected to a computer and Arduino IDE:
* remove the original ATmega328P-PU chip from the Arduino board;
* insert the target ATmega328P-PU chip into the Arduino board;
* connect the Arduino board to a computer using a USB cable;
* upload scketch into the target using Arduino IDE;
* disconnect the Arduino board from the computer;
* remove the target ATmega328P-PU chip for standalone use and reinsert the original ATmega328P-PU chip into the Arduino board.

Note. Be sure that no power supply (USB cable or external power supply) is connected when manipulating chips.

## 6.Code

For quick testing use blink.ino sketch (from the included examples in Arduino IDE).

## 7. Demo

Youtube link: [Standalone ATmega328 w Reset Button and LED](https://www.youtube.com/watch?v=FxPCljKBedM)

## 8. Additional resources

* References:
    * From Arduino to a Microcontroller on a Breadboard: https://www.arduino.cc/en/Tutorial/ArduinoToBreadboard
    * Building an Arduino on a Breadboard: https://docs.arduino.cc/retired/hacking/hardware/building-an-arduino-on-a-breadboard/
    * Pololu 5V Step-Up/Step-Down Voltage Regulator S7V7F5: https://www.pololu.com/product/2119
    * Atmel ATmega328-328P_Datasheet:
    https://ww1.microchip.com/downloads/en/DeviceDoc/ATmega48A-PA-88A-PA-168A-PA-328-P-DS-DS40002061A.pdf