# MQTTDevice

MQTTDevice is an Arduino sketch for the ESP32 Wemos D1 mini modules. MMQTTDevice enables sensors, actors and an induction hob GGM IDS2 to be communicate via WLAN and MQTT with [CraftBeerPi V4](https://github.com/avollkopf/craftbeerpi4).

The instructions on MQTTDevice gitbook apply to both modules, ESP32 and ESP8266. MQTTDevice32 offers more GPIOs and a faster CPU than MQTTDevice4. Please note some syntax differences when flashing firmware.

Please support the MQTTDevice project and expand this short manual, FAQs, languages etc.

![Web Interface](img/startseite.jpg)

## 🗺️ Multilingual

MQTTDevice supports different languages. Each language has its own language file. The language files in JSON format are stored in the data folder.

_Supported the project and translate MQTTDevice into a new language or corrected existing language files!_

## 💠 GPIO mapping ESP32

The ESP32 D1 offers a pinout suitable for the ESP8266 (GPIO D0 to D8). The pin assignment shown is based on the ESP32 D1 Mini NodeMCU module from [AZ-Delivery](https://www.az-delivery.de/products/esp32-d1-mini)

GPIO mapping:

![ESP32 D1 Pinout-1](/docs/img/ESP32-D1.pinout-1.jpg)
![ESP32 D1 Pinout-2](/docs/img/ESP32-D1.pinout-2.jpg)

| Name |   GPIO   |  Input  |  Output  | Description |
| ---------- | -------- | ------- | -------- | ------------ |
|     D0     |  GPIO026 |   ok    |   ok     |              |
|     D1     |  GPIO022 |   ok    |   ok     | SCL Display  |
|     D2     |  GPIO021 |   ok    |   ok     | SDA Display  |
|     D3     |  GPIO017 |   ok    |   ok     | DS18B20 sensors |
|     D4     |  GPIO016 |   ok    |   ok     |              |
|     D5     |  GPIO018 |   ok    |   ok     | IDS2 blue    |
|     D6     |  GPIO019 |   ok    |   ok     | IDS2 yellow  |
|     D7     |  GPIO023 |   ok    |   ok     | IDS2 white   |
|     D8     |  GPIO005 |   ok    |   ok     | MAX31865 CS5, Buzzer |
|     D9     |  GPIO027 |   ok    |   ok     | MAX31865 SCLK |
|     D10    |  GPIO025 |   ok    |   ok     | MAX31865 MISO |
|     D11    |  GPIO032 |   ok    |   ok     | MAX31865 MOSI |
|     D12    |  GPIO012 |  (ok)   |   ok     | TDI, boot fails if pulled high, strapping pin |
|     D13    |  GPIO004 |   ok    |   ok     | MAX31865 CS0 |
|     D14    |  GPIO000 | pullUp  |  (ok)    | must be low to enter flash mode |
|     D15    |  GPIO002 |   ok    |   ok     | onboard LED, must be low to enter flash mode |
|     D16    |  GPIO033 |   ok    |   ok     | MAX31865 CS1 |
|     D17    |  GPIO014 |   ok    |   ok     | MAX31865 CS2 |
|     D18    |  GPIO015 |   ok    |   ok     | MAX31865 CS3 |
|     D19    |  GPIO013 |   ok    |   ok     | MAX31865 CS4 |

Pins connected to onboard flash and not recommended for GPIO use:
CMD (IO11), CLK (IO6), SD0/SDD (IO7), SD1 (IO8), SD2 (IO9) and SD3 (IO10)

## 💠 GPIO mapping ESP8266

| Bezeichner |   GPIO   |  Input  |  Output  | Beschreibung |
| ---------- | -------- | ------- | -------- | ------------ |
|     D0     |  GPIO026 |   ok    |   ok     | MAX31865 MOSI (High at boot, no int, no PWM) |
|     D1     |  GPIO022 |   ok    |   ok     | SCL Display, MAX31865 MISO  |
|     D2     |  GPIO021 |   ok    |   ok     | SDA Display, MAX31865 CLK  |
|     D3     |  GPIO017 |   ok    |   ok     | DS18B20 sensors |
|     D4     |  GPIO016 |         |   ok     | MAX31865 CS0 (High at boot, onboard LED)|
|     D5     |  GPIO018 |   ok    |   ok     | IDS2 blue, MAX31865 CS1   |
|     D6     |  GPIO019 |   ok    |   ok     | IDS2 yellow, MAX31865 CS2 |
|     D7     |  GPIO023 |   ok    |   ok     | IDS2 white |
|     D8     |  GPIO005 |         |   ok     | Buzzer       |
