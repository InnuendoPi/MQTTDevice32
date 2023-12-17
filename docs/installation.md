# Installation

The installation is divided into three steps:

1. Installation of RaspberryPi and CraftbeerPi4
2. Installation MQTT Broker
3. Installation MQTTDevice

The installation and configuration of CraftbeerPi4 is described here: <https://openbrewing.gitbook.io/craftbeerpi4_support/master/server-installation>
You will need version 4.0.1.11 or above. Earlier versions do not support MQTT actors.

The installation and configuration of RaspberryPi is available in many good instructions on the internet.

The communication between CraftbeerPi and MQTTDevice takes place via WLAN. Sensors send temperature values ​​to CraftbeerPi and CraftbeerPi sends commands to actors (e.g. switch agitator on / off). The MQTT protocol is used for this communication. The MQTT protocol requires a MQTT broker.
