# GPIO I2C pHAT

<p align="center">
    <a href="https://plasmadan.com/gpioi2c?utm_source=github&utm_medium=banner" target="_blank" rel="nofollow">
        <img alt="GPIO I2C pHAT" src="/img/gpio-i2c-phat.jpg" width="500">
    </a>
</p>

## Usage

Add required dtoverlay parameter(s) to ```/boot/config.txt``` and reboot.

| Switch Position | Hardware I2C (Pi 4) | Software I2C (Bit Bang) | GPIO |
| :---: | :---: | :---: | :---: |
| I2C3 | dtoverlay=i2c3 | dtoverlay=i2c-gpio,bus=3,i2c_gpio_sda=4,i2c_gpio_scl=5 | 4 5 |
| I2C4 | dtoverlay=i2c4 | dtoverlay=i2c-gpio,bus=4,i2c_gpio_sda=8,i2c_gpio_scl=9 | 8 9 |
| I2C5 | dtoverlay=i2c5 | dtoverlay=i2c-gpio,bus=5,i2c_gpio_sda=12,i2c_gpio_scl=13 | 12 13 |
| I2C6 | dtoverlay=i2c6 | dtoverlay=i2c-gpio,bus=6,i2c_gpio_sda=22,i2c_gpio_scl=23 | 22 23 |

Note: When using multiple software I2C buses, add the parameters from highest to lowest, i.e., 6, 5, 4, 3.

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
