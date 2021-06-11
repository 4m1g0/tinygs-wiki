* **The config panel asks for user and password!!**
The user is always `admin` and the password is the password you configured during the setup process on the config panel itself. Read more on the [Ground Station configuraton page](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).

* **I don't remember the password of the config panel!!**
 Don't worry, you can recover your password with one of these methods:
    1) At any time press the _PROG_BUTTON_ of your board or connect the _PROG_BUTTON pin_ to GND for 8 seconds to enter _Rescue Mode_. In rescue mode your ground station will generate an AP with the name of your station without password and you will be able to use that AP to change the config, including your passwords. The PROG_BUTTON pin depends on the board you are using and it is defined by the [board template](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).
    2) Connect to the serial port of the board using your favourite serial monitor (Platformio, Ardino, Putty...) 115200 baud and send a character 'e'. This will reset your board to default parameters.  
    4) Using Platform.io erase the ESP32 flash memory with: `pio run --target erase`
    5) Use the [One click Uploader](https://github.com/G4lile0/tinyGS/wiki/Quick-Start) to reinstall the firmware.

After this you will need to connect to the tinyGS config AP and set all the parameters. Read more on the [Ground Station configuration page](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).

* **How can I get the user and password for the MQTT server?**
We use [Telegram](https://telegram.org/) as the main communication channel. Join our 
[Community Chat](https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q)  After joining the channel, look or search for 
the "TinyGS Personal Bot" (It usually sends a welcome message to new members). Sent a message of "/mqtt" and the bot will respond with your
MQTT credentials.  

* **I'm new and I want to get in, what hardware should I buy?**
First choose the satellites that you want to receive. We recommend 433Mhz since there are more satellites. Also, some satellites like V-R3x only work in 915Mhz band and we expect more in the future. However, recently all 915 satellites become inactive, so it's unlily to receive them in the near future.

* **I have a LoRa Board with frequency 433, 868 or 915 MHz can I use it in a different band?**
Other frequencies wont make the firmware fail but you will probably not be able to receive anything from the satellite, due the matching RF circuits.

* **What type of antenna should I use for TinyGS**
LoRa is an awesome technology and can receive signals under the noise floor. The standard duck or coil antennas that usually come with Heltec or TTGO boards were proven to receive some packets from quite long distances. However, the conditions have to be good to be able to receive with such antennas. In order to have a more reliable groundStation we recommend to build a better tiny antenna. You can read more about the different options on the [Antennas page from @judhi](https://github.com/G4lile0/tinyGS/wiki/Antennas).

* **I receive a lot of packets that appear as "Unknown" on the tinygs.com website**
Some satellites transmit on frequencies that are used for other things on earth. Some even use standard LoRa frequiencies so it's normal that not everything that your station receive is from a satellite. Our system is capable of detecting the structure of the packets from the supported satellites, so if a frame is marked as "Unknown" it's probably a terrestrial LoRa packet or interferences from other technologies.

* **MQTT connection failed with error: failed, rc=-2**
The ground station could not connect to the MQTT server. Check your connection and make sure there is nothing blocking the connection such as a firewall or content blocker. Some users have reported problems with [pihole](https://pi-hole.net/). Adding an exception should solve the problem.

* **Screen OLED inverted**
The OLEd display changes depending on the hour: during the day is white and during the night is black. This change
protects the OLED by changing the lit pixels from time to time, otherwise some pixels may burn out sooner. Disabling this feature is not recomended as it will increase the wearout of your display but you can disable it using the advanced parameters setting `dnOled` to true. Example: `{"dnOled":true}`

* **What does CRC error mean and why doesn't it appear as a received packet**
The Cyclic Redundancy Check (CRC) verifies the integrity of the received packet. Some packets with CRC errors are expected. The LoRa demodulation can find packets despite a lot of noise. Some false positive results are expected and in some receiver configuration we may receive a lot. The CRC check is a filter for these packets, but they are not necessarily an indicator of bad hardware.

* **Why can't I access to the MQTT server as I did before?**
Check the [Programmatic API](https://github.com/G4lile0/tinyGS/wiki/Programmatic-API) for a more in depth explanation.




