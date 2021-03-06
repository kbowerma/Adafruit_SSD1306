Adafruit_SSD1306
================

Adafruit_SSD1306 library ported for Spark by Paul Kourany, Mar 18, 2014

## Software SPI

SSD1306 128x64 Wiring guide

```
// If using software SPI (the default case):
#define OLED_MOSI   D0
#define OLED_CLK    D1
#define OLED_DC     D2
#define OLED_CS     D3
#define OLED_RESET  D4
Adafruit_SSD1306 display(OLED_MOSI, OLED_CLK, OLED_DC, OLED_RESET, OLED_CS);
```
<img src="SSD1306-128x64.jpg" alt="SSD1306 128 x 64 wiring guide"/>



.
.
.

Update by Jeremy Ellis Feb 9th, 2016

If using the beginner-128x64-OLED-I2C.ino with the particle.io and the I2C protocol and the Grove seeedstudio 128x64 OLED

http://www.seeedstudio.com/wiki/Grove_-_OLED_Display_0.96%22#With_Arduino



you can connect all four wires to the Photon

1. black GND 
1. red 3v3      
1. white SDA   Pin D0 
1. yellow SCL  Pin D1 

Remember to include the following files:

1. Adafruit_GFX.cpp
1. Adafruit_GFX.h
1. Adafruit_SSD1306.cpp
1. Adafruit_SSD1306.h

## Hardware SPI

If your OLED screen has the following labels: `CS`, `DC`, `RST`, `D1`, `D0`, `VCC`, `GND` you have a Hardware SPI and should use `ssd1306_128x64_spi.ino`

The wiring should match this:

```
OLED_D0 -> A3 (SPI CLK)
OLED_D1 -> A5 (SPI MOSI)
OLED_DC -> D3
OLED_CS -> D4
OLED_RESET -> D5
OLED_VCC -> 3V3
OLED_GND -> GND
```

Tested on Particle Photon.

Compiled from https://community.particle.io/t/adafruit-ssd1306-solved/15175/26
