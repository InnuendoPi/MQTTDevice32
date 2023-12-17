# Updates

The firmware offers two options for installing updates very easily.

1. Firmware Update file upload

    Call up the URL <http://mqttdevice/update> in the web browser or use the "Update" -> "Upload" button in the WebIf.
    Firmware and the LittleFS file system can be updated here. If the file system LittleFS is updated with file upload, the configuration file is overwritten. See backup and restore.

2. WebUpdate

    Open the webfront of your MQTTDevice in your web browser and call the "Update" -> "WebUpdate" function.
    WebUpdate updates the firmware, the index file and certificates. The configuration file is not overwritten by WebUpdate.

The WebUpdate can take a few minutes, depending on your internet connection. The web interface is not available during the web update. If only a very slow internet connection is available, the message "Browser not responding" is displayed after approx. 60 seconds. Please wait and let the WebUpdate run through.
