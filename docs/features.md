# ✅ Features

* Web Interface (WebIf) for easy configuration, backup and restore
* Server Sent Events (SSE) for WebClients
* Temperature sensors
  * Dallas DS18B20 Sensors (digital)
    * Search for connected sensors based on OneWire addresses
  * PT100 and PT1000 sensors (analog)
    * MAX31865 Amplifyer
  * MQTTDevice32 supports max 6 sensors
  * MQTTDevice4 supports max 3 sensors
* Actors (max 15)
  * GPIO selection
  * used GPIOs are hidden
  * inverted GPIO
  * PWM values ​​between 0 and 100% are sent. MQTTDevice "pulses" with a cycle of 1000ms
  * MQTTDevice32 supports up to 15 actors
  * MQTTDevice4 supports 10 actors
* Induction hob
  * induction hob GGM IDS2 can be controlled directly
* Nextion HMI Touchdisplay support
* Audio signals Piezo Buzzer
* WebUpdate firmware
* mDNS support
* Event handling
* File explorer
* support for different languages
