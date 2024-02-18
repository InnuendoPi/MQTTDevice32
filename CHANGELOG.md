# Changelog

Version 4.59a

- Update:     ArduinoJSON API 7
- Reworked:   JSON handling: removed all nested objects and arrays (API 7)
- New:        Parameter Display CBPi4 Fermenter
- Changed:    MQTT Callback
- Changed:    subscribe to fermenter topics if enabled
- New:        Parameter dutycycle
- Changed:    Filtering MQTT payloads

Version 4.58b

- Fix:        WebUpdate FrameWork
- Changed:    Default WLAN name in AP Mode changed to MQTTDevice
- Changed:    Reset to factory default (clear config and WLAN settings enabled)
- Fix:        max number of sensors allowed
- Fix:        dyn. increase sensor update intervall fitting number of configured sensors
- Fix:        Reload WebIf after reboot failed
- Fix:        ESP32 mDNS webservice
- Fix:        close modal windows after config restore and reboot
- Changed:    reboot function
- Changed:    Merged source ESP8266 in ESP32 using compiler directives
- Changed:    Rebuild WebIf
- Changed:    Restore config file
- Optimzed:   reduce amount of data transfered to connected clients
- New:        language switch (en, de)
- New:        Mouseover tooltips
- Changed:    select handle sensor type and sensor pins
- Changed:    IDS Pin Interrupt
- Fix:        long sensor/actor names
- Fix:        long mqtt topics
- Fix:        HMI display mDNS name
- Changed:    Added ".local" to mDNS hints, views and docs
- New:        Added Max31865 Amplififer SPI support (PT100/PT1000 support) MOSI: D0 MISO: D1 SCLK: D2 CS: D4/D5/D6
- New:        Added PT100/1000 sensor support
- Changed:    max number of sensors 3
- Fix:        Remove last sensor/actor did not refresh WebIf table
