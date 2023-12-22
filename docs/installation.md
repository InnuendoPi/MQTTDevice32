# Installation

While installation of MQTTDevice is very easy you need some prerequisite.

## Prerequisite CraftbeerPi4

The installation and configuration of CraftbeerPi4 is described here: <https://openbrewing.gitbook.io/craftbeerpi4_support/readme/server-installation>. Version 4.0.1.11 or above is required. Earlier versions do not support MQTT actors.

## Prerequisite MQTT Broker

The MQTT protocol is used for communication between CraftbeerPi and MQTTDevice. Sensors send temperature values ​​to CraftbeerPi and CraftbeerPi sends commands to actors (e.g. switch agitator on / off). The MQTT protocol requires a MQTT broker. Please follow the instructions on craftbeerpi gitbook to install and configure a MQTT broker like mosquitto: <https://openbrewing.gitbook.io/craftbeerpi4_support/readme/craftbeerpi-4-server/mqtt-connectivity>
