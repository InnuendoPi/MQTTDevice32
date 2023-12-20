# Updates

The firmware offers two options for installing updates very easily.

1. Firmware Update file upload

    Open URL <http://mqttdevice/update> in your web browser or use the "Update" -> "Upload" button in the WebIf.
    Firmware and the LittleFS file system can be updated.

    _Note: Filesystem update will overwrite device configuration._

2. WebUpdate

    Open the webfront of your MQTTDevice in your web browser and select "Update" -> "WebUpdate" function.
    WebUpdate updates the firmware and framework files. The device configuration will not be overwritten by WebUpdate.

The WebUpdate can take a few minutes, depending on your internet connection. The web interface is not available during the web update. If only a very slow internet connection is available, the message "Browser not responding" is displayed after approx. 60 seconds. Please wait and let the WebUpdate run through.
