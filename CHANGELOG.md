# Changelog

Version 4.63

- Fix:        missing LF (\n) in SSE broadcasts
- Changed:    Avoid Strings in SSE and html response
- Revert:     ESP-IDF v4.4.7
- Update:     Arduino CLI 1.0.4
- Update:     InnuTicker 0.0.4

Version 4.62

- Update:     ArduinoJSON 7.1.0
- Fix:        Arduino core: set back Pin signal polarity (#9952)
- Update:     ESP-IDF v4.4.8 final
- Update:     Arduino CLI 1.0.2

Version 4.61c

- Update:     ESP32 core 2.0.17 ESP-IDF v4.4.7
- Update:     VSCode 1.89
- Changed:    Actors,IDS2 update intervall 1000ms

Version 4.61b

- Update:     ESP32 core 2.0.16 ESP-IDF v4.4.7

Version 4.61a

- Fix:        ESP32 error loading WebIf (sometimes WebIf incomplete, icons missing, ESP32 reboot after 20sec due to no answer web requests)
- Optimize:   Load WebIf ESP32
- Update:     ESP32 core 2.0.15 ESP-IDF v4.4.7
- Update:     ESPtool 4.7.0
- Update:     VSCode 1.88

Version 4.60

- New:        Parameter senCycle for CBPi4 fermenter mode (leave default 1 second)
- Changed:    Fermenter topics. CraftBeerPi 4.3.2 or newer required
- Update:     Lib ArduinoJSON 7.0.4

Version 4.59

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
