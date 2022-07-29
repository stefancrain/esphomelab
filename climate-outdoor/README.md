# Climate Outdoor

Climate / Air Quality / Lightning monitor to be deployed outside.

## BOM

- [LILYGO® T8 V1.7.1 ESP32](https://www.aliexpress.com/item/2251832665108663.html)
  - [Image](https://github.com/LilyGO/TTGO-T8-ESP32/blob/master/image/T81.7.jpg)
  - [Schematic](https://github.com/LilyGO/TTGO-T8-ESP32/blob/master/t8_v1.7.1.pdf)
- Sensors
  - AS3935
    - Lightning Energy
    - Storm Distance
  - BME680
    - Temperature
    - Pressure
    - Humidity
    - IAQ
    - CO2 Equivalent
    - Breath VOC Equivalent
  - PMS5003
    - pm_1_0
    - pm_2_5
    - pm_10_0
  - DS18B20
    - Temperature
- [Adafruit Lithium Ion Battery Pack - 3.7V 6600mAh](https://www.amazon.com/dp/B0137IPVY6)
- [ZUMIMALL 5v Solar Panel](https://www.amazon.com/gp/product/B07V5N5C2L)

## Gotchas

- CHECK YOUR POLARITY!
  - Adafruit battery connector uses a JST 2.
  - The LILYGO T8 1.7.1 uses a JST 1.2
  - Adafruit batteries are Reversed polarity to the T8 plugs.
  - **Solder up a quick conversion cable**
    - I let magic smoke out with my first JST 2.0 -> 1.2 converter
