# GPIO I2C pHAT

The GPIO I2C pHAT is an I2C switch for Raspberry Pi which remaps the I2C bus (pins 3 & 5) to 1 of 4 additional buses, allowing any I2C based add-on board to use an alternative I2C bus, without the need for multiplexers or expanders.

Makes use of the extra hardware I2C buses introduced on Raspberry Pi 4 (BCM2711) or software I2C (bit bang). Switching is controlled using a 4-position double-pole slide switch, which allows you to quickly switch between buses.

Multiple GPIO I2C boards can be stacked along with other HATs or pHATs, and it's fully compatible with our [HAT RACK](https://github.com/plasmadancom/HAT-RACK) mounting boards.

Includes a breakout header for the 4 extra I2C buses. These are always connected to the associated GPIO pins so can be used regardless of the switch position. Note: external pull-up resistors to 3.3V required.


## Features

* Adds 4 additional I2C buses with breakout
* User selectable I2C GPIO pin remapping
* Slide switch allows fast bus switching
* No-conflict solder jumpers
* Stackable design
* Immersion gold plated copper
* UL, CE, UKCA and RoHS (lead free) compliant


## Usage

Add required dtoverlay parameter(s) to ```/boot/config.txt``` and reboot.

| Switch Position | Hardware I2C (Pi 4) | Software I2C (Bit Bang) | GPIO |
| :---: | :---: | :---: | :---: |
| I2C3 | dtoverlay=i2c3 | dtoverlay=i2c-gpio,bus=3,i2c_gpio_sda=4,i2c_gpio_scl=5 | 4 5 |
| I2C4 | dtoverlay=i2c4 | dtoverlay=i2c-gpio,bus=4,i2c_gpio_sda=8,i2c_gpio_scl=9 | 8 9 |
| I2C5 | dtoverlay=i2c5 | dtoverlay=i2c-gpio,bus=5,i2c_gpio_sda=12,i2c_gpio_scl=13 | 12 13 |
| I2C6 | dtoverlay=i2c6 | dtoverlay=i2c-gpio,bus=6,i2c_gpio_sda=22,i2c_gpio_scl=23 | 22 23 |

Note: When using multiple software I2C buses, add the parameters from highest to lowest, i.e., 6, 5, 4, 3.

## Device Compatibility

GPIO I2C pHAT is compatible with all **40-way** Raspberry Pi models.

| Device Model | Compatibility |
| --- | :---: |
| Raspberry Pi 1 Model A+/B/B+ | &#x2714;&#xFE0F; |
| Raspberry Pi 2 Model B | &#x2714;&#xFE0F; |
| Raspberry Pi 3 Model B+ | &#x2714;&#xFE0F; |
| Raspberry Pi 4 | &#x2714;&#xFE0F; |
| Raspberry Pi Zero | &#x2714;&#xFE0F; |

## Dimensions

<p align="center">
    <a href="https://raw.githubusercontent.com/plasmadancom/GPIO-I2C-pHAT/main/img/gpio-i2c-phat-v1.0-dimensions.svg">
        <img alt="Mechanical Drawing" src="/img/gpio-i2c-phat-v1.0-dimensions.svg" width="600">
    </a>
</p>

## References

https://github.com/raspberrypi/firmware/tree/master/boot/overlays

## Product Data

MPN: GPIO-I2C-PHAT  
EAN: 0616908588436

## License

MIT © Dan Jones - [PlasmaDan.com](https://plasmadan.com)
