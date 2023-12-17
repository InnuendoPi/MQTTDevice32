# Flash firmware

With the help of esptool.exe (<https://github.com/igrr/esptool-ck/releases>) in the github tools subfolder, the firmware can be flashed onto the ESP module. The ESPTool is available for different operating systems.
ESPtool-ck Copyright (C) 2014 Christian Klippel <ck@atelier-klippel.de>. This code is licensed under GPL v2.

The USB driver CH341SER is required under Win10: <http://www.wch.cn/download/CH341SER_ZIP.html>

Example for an ESP8266 module of the type Wemos D1 mini with 4MB Flash connected via USB as COM3

* Download the Firmware.zip archive from the tools folder on github and extract it to any folder

  * The archive contains the esptool for flashing, the Flashen.cmd script and the two firmware files

  * Double click on the file Flashen.cmd.

  The firmware is now installed on the MQTT device.

  *The Flash script uses COM3 as the connection for the MQTTDevice. If COM3 is not the correct port for the Wemos D1 mini, COM3 must be replaced by the correct port in two places in the Flashen.cmd script.*

  After flashing, the MQTT device starts in access point mode with the name "ESP8266-xxxx" und address <http://192.168.4.1>

![wlan](img/wlan-ap.jpg)

The MQTT device must now be connected to the WLAN.

The MQTT sensor "Induction temperature" and the MQTT actor "Agitator" are now created on the MQTTdevice with the identical CBPi4 topics:

![mqttSensor2](img/mqttSensor2.jpg)

![mqttAktor2](img/mqttAktor2.jpg)

The sensor or actor name can be different. These steps complete the exemplary installation and configuration of MQTT sensors and actors. Up to 6 sensors and 8 actors can be set up per MQTT device. (Almost) any number of MQTT devices can be connected to CraftbeerPi via MQTT. Three MQTT devices are used very often:

MQTTDevice 1: Mash tun with temperature sensors and agitator.

MQTTDevice 2: HLT with temperature sensors, pumps and valves etc.

MQTTDevice 3: Fermenter with temperature sensors, an actor for heating and an actor for cooling

Any combination is possible. Because the MQTT communication is implemented via topics, a temperature sensor and an induction hob for a CraftbeerPi Kettle do not have to be configured on the same MQTTDeivce.

![induction](img/induction.jpg)

The picture above is an example on how to configure an induction hob GGM IDS2. Do not reduce fan run on after power off below 120sec: savely cool down induction hob after mash or boil. GPIOs D5, D6 and D7 are highly recommended. Check ESP8266 manual for further information about GPIO states (High/Low) on startup.
