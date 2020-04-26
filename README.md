# HC-18-BLE
An Arduino library for the HC-18 Bluetooth module from DSD TECH using the CC2640 chip. Made for version "HM10-V111" firmware, but might work with others.

## Background
This code is based on the orginal from dennistreysa/HC-06-BT

## Config
There is not much you can configure. A minimal setup looks like the following:

```c++
Bluetooth BT(2, 3); // RX, TX
```

If you want to, you can specify the baudrate of the controller:

```c++
Bluetooth BT(2, 3, 9600); // RX, TX
```

## Limitations
As you can read [here](https://www.arduino.cc/en/Reference/SoftwareSerial) there are some limitations to the SoftwareSerial:

* If using multiple software serial ports, only one can receive data at a time.
* Not all pins on the Mega and Mega 2560 support change interrupts, so only the following can be used for RX: 10, 11, 12, 13, 14, 15, 50, 51, 52, 53, A8 (62), A9 (63), A10 (64), A11 (65), A12 (66), A13 (67), A14 (68), A15 (69).
* Not all pins on the Leonardo and Micro support change interrupts, so only the following can be used for RX: 8, 9, 10, 11, 14 (MISO), 15 (SCK), 16 (MOSI).
* On Arduino or Genuino 101 the current maximum RX speed is 57600bps
* On Arduino or Genuino 101 RX doesn't work on Pin 13

## Resources

* [DSD TECH DataSheet](https://drive.google.com/file/d/1tKEwk9f0gSQ1rSV3ei9nNnNElQzgrnN0/view?usp=sharing)

## Other Libraries

* [Android with Arduino - Bluetooth](https://github.com/aron-bordin/Android-with-Arduino-Bluetooth) by aron-bordin
* [PNG-Arduino-Framework-master](https://github.com/aron-bordin/PNG-Arduino-Framework) by aron-bordin
