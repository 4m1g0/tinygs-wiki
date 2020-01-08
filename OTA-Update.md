This project implements OTA updates with both Arduino IDE and Platformio. To use this flashing method the board and the computer have to be connected to the same network and be visible to each other.

## Platformio
In order to upload a new version through OTA in platformio, the `platformio.ide` file has to be edited uncommenting two lines to enable OTA and set the current IP Address of the station (it can be seen on the OLED display).

```
# Uncomment these 2 lines by deleting ";" and edit as needed to upload through OTA
;upload_protocol = espota
;upload_port = IP_OF_THE_BOARD
```

Once this is done, the new firmware can be uploaded using the upload button normally as if the board were connected through USB.

## Arduino IDE
To upload a new version through OTA on Arduino, you have to navigate to `Tools > port` and, if the computer is in the same network it should detect a network port for the ESP32. If that is the case, select the network port.

Once this is done, the new firmware can be uploaded normally using the upload button or navigating to `Program > upload`
