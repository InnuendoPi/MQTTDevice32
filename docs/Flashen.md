# ▶️ Flash firmware

With the help of esptool.exe (<https://github.com/espressif/esptool>), the firmware can be flashed onto the ESP module. The ESPTool is available for different operating systems. ESPTool is licensed under GPL v2.

The USB driver CH341SER is required under Win10/11: <http://www.wch.cn/download/CH341SER_ZIP.html>

Example for an ESP8266 module of the type Wemos D1 mini with 4MB Flash connected via USB as COM3

* Download the Firmware.zip archive from the tools folder on github and extract it to any folder

  * The archive contains the esptool for flashing, the Flashen.cmd script and the two firmware files

  * Double click on the file Flashen.cmd.

  The firmware is now transfered into MQTTdevice flash.

## Manual flash firmware

Linux users must download esptool and flash firmware manual

ESP32 modules:

```bash
esptool.exe --chip esp32 erase_flash
echo Flash firmware and LittleFS 
esptool.exe --chip esp32 --before default_reset --after hard_reset write_flash 0x1000 MQTTDevice32.ino.bootloader.bin 0x8000 MQTTDevice32.ino.partitions.bin 0xe000 boot_app0.bin 0x10000 MQTTDevice32.ino.bin 0x2b0000 MQTTDevice32.mklittlefs.bin
```

ESP8266 modules

```bash
esptool.exe --chip esp8266 erase_flash
esptool.exe --chip esp8266 write_flash MQTTDevice.ino.bin 0x200000 MQTTDevice.mklittlefs.bin
```

## Flash Firmware macOS

Download: [pyflasher](https://github.com/marcelstoer/nodemcu-pyflasher/releases)

Step 1: flash firmware MQTTDevice.ino.bin

![macOS](img/flashen_macos.png)

Step 2: connect device with your WLAN

Step 3: open file update on MQTTDevice: <http://mqttdevice.local/update> choose filesystem and upload MQTTDevice.mklittlefs.bin

## Configure WLAN

After flashing, the MQTT device starts in access point mode with an open WLAN named "MQTTDevice" and IP address <http://192.168.4.1>

![wlan](img/wlan-ap.jpg)

The MQTT device must now be connected to the WLAN.
