# LCD-I2C
C++ Library for Liquid Crystal Displays (LCD) with the Hitachi HD44780 display driver.
The communication is realized by a PCF8574 remote 8 bit I/O Expander for I²c Bus.

![LCD](./docs/LCD_Display.PNG)

## Contents
* [LCD Documentation](#lcd-documentation)
* [Library Usage](#library-usage)
* [License](#license)
* [Helpful Links](#helpful-links)


## LCD Documentation
### Hitatchi HD44780
The Hitachi HD44780 LCD controller is an alphanumeric dot matrix liquid crystal display (LCD) controller developed by Hitachi in the 1980s. The character set of the controller includes ASCII characters, Japanese Kana characters, and some symbols in two 40 character lines. Using an extension driver, the device can display up to 80 characters. Numerous third-party displays are compatible with its 16-pin interface and instruction set, making it a popular and cheap LCD driver.

In 8-bit mode, all transfers happen in one cycle of the enable pin (E) with all 8 bits on the data bus and the RS and R/W pins stable. In 4-bit mode, data are transferred as pairs of 4-bit "nibbles" on the upper data pins, D7–D4, with two enable pulses and the RS and R/W pins stable. The four most significant bits (7–4) must be written first, followed by the four least significant bits (3–0). The high/low sequence must be completed each time or the controller will not properly receive further commands.

### Character Generator ROM (CGROM)
The internal CGROM includes 208 charaters in a 5x8 dot matrix, and also 32 characters in a 5x10 dot matrix.
The 5x10 matrix is generally not used.

### Character Generator RAM (CGRAM)
Additionally to the CGROM there is a CGRAM, in which 8 user-defined characters in 5x8 dot matrix, or 4 characters in a 5x10 dot matrix can be stored. 
This enables to store characters which are not available in the CGROM.

## Library Usage

# License
This library is licensed under MIT Licence.

[LCD-I2C lisence](https://github.com/hasenradball/LCD-I2C/blob/master/LICENSE)

# Helpful Links
[Wikipedia - a great description of HD44780 module](https://de.wikipedia.org/wiki/HD44780)

