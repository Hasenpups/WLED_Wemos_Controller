Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


## Donations / Spenden
If somebody wants to support me for upcoming projects :)  
- PayPal:  [![donate](https://www.paypalobjects.com/de_DE/DE/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donate/?hosted_button_id=T25NKW8BXJ7J8)
- Amazon Giftcard: https://www.amazon.de/Amazon-Gutschein-per-E-Mail-Amazon/dp/B0054PDOV8 - stefan.riese@me.com

# WLED controller board for D1 mini (Wemos)
This board is designed to connect addressable LEDs/Neopixel strips and handle them with the WLED firmware. Other firmware can be used as well.

## Features
- preflashed with WLED
- 5V/GND connector for input voltage
- 5V/GND connector for LED strip
- up to 3 data lines with ESP8266
- up to 4 data lines with ESP32
- support for LED strips with clock signal
- level shifter for LED signals (3.3V -> 5V )
- connector for microphone sensor or button input (3.3V, GND, A0)
- resistor for data lines if necessary
- capacitor to stabilize input voltage

## BOM / Kit
- 1 x PCB
- 1 x Wemos D1 mini (https://www.amazon.de/gp/product/B08BTH77F3)
- 1 x 330 Ohm Widerstand (R4 SMD or R4_1 wired)
- 1 x 2-pin screw terminal (https://www.amazon.de/gp/product/B08JB6SSCJ)
- 1 x 4-pin screw terminal (https://www.amazon.de/gp/product/B08JB6SSCJ)
- 1 x SN74AHCT125N level shifter (https://www.berrybase.de/bauelemente/aktive-bauelemente/ics/ics-s../sn74ahct125n-quad-level-shifter-dil-14)
- 1 x Capacitor 1000µF 10V 10mm (https://www.ebay.de/itm/321955917188)

![Alt text](./images/IMG_7098.jpeg?raw=true "content")

## Wiring diagram
- https://github.com/Hasenpups/WLED_Controller/blob/main/WLED_Controller.pdf

## Assembly
- Solder R4 SMD 330 Ohm or R4_1 wired 330 Ohm
- (optional) Solder R1-R3 330 Ohm if multiple data lines are used
- (optional) Bridge JP1 if 4 pin LED strip is used with clock (CLK) signal
- Solder level shifter
- Solder screw terminals
- (optional) Solder JST connector for additional sensor or button
- Solder capacitor
- Solder D1 mini with female headers on the board and male pins on the D1 mini (pluggable) or directly with long male headers on the D1 mini to the PCB

![Alt text](./images/IMG_7087.jpeg?raw=true "solder1")
![Alt text](./images/IMG_7088.jpeg?raw=true "solder2")
![Alt text](./images/IMG_7089.jpeg?raw=true "solder3")
![Alt text](./images/IMG_7090.jpeg?raw=true "solder4")
![Alt text](./images/IMG_7091.jpeg?raw=true "solder5")
![Alt text](./images/IMG_7092.jpeg?raw=true "solder6")
![Alt text](./images/IMG_7093.jpeg?raw=true "solder7")

## Software
- WLED - https://github.com/Aircoookie/WLED/releases
- Sound Reactive WLED - https://github.com/atuline/WLED/releases

## WLED configuration

![Alt text](./images/Output_config.png?raw=true "outputConfig")

### ESP8266
- Data line 1 - IO14
- Data line 2 - IO12
- Data line 3 - IO13
- Data line 4 - IO15

### ESP32
- Data line 1 - IO18
- Data line 2 - IO19
- Data line 3 - IO25
- Data line 4 - IO5

## Case
https://www.thingiverse.com/thing:5189346
