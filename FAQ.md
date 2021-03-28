* **The config panel asks for user and password!!**
The user is always `admin` and the password is the password you configured during the setup process on the config panel itself. Read more on the [Ground Station configuraton page](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).

* **I don't remember the password of the config panel!!**
 Don't worry, you can reset to default parameters though one of four methods: 
    1) Use a serial terminal application, such Putty or Termite on Windows or minicom/miniterm on Linux.  
       Connect the device to your computer via USB cable. Determine which USB/serial port. Using serial settings of
       115,200 baud, 8 data bit, N parity, 1 stop.  Hit the key `e` on the keyboard 
    2) Push and Hold the user button for 5 seconds the credits screen shown on the OLED during booting. 
    3) Rest the GS 10 times within 30 seconds 
    4) Using Platform.io to reflash the firmware onto the device.

    After this you will need to connect to the tinyGS config AP and set all the parameters. Read more on the [Ground Station configuration page](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).

* **How can I get the user and password for the MQTT server?**
We use [Telegram](https://telegram.org/) as the main communication channel. Join our 
[Community Chat](https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q)  After joining the channel, look or search for 
the "TinyGS Personal Bot" in the list of channel members. Sent a message of "/mqtt" and the bot will respond with your
MQTT credentials.  

* **I'm new and I want to get in, what hardware should I buy?**
Fist choose the satellites that you want to receive. We recommend 433Mhz since there are more satellites, but
check your local radio regulations. Also, some satellites like V-R3x only work in 915Mhz band. There are two main types of lora chips SX127X and SX126X. 

* **I have a LoRa Board with frequency 433, 868 or 915 MHz can I use it in a different band**
Other frequencies wont make the firmware fail but you will probably not be able to receive anything from the satellite, due the matching circuits.

* **MQTT connection failed with error: failed, rc=-2**
The ground station could not connect to the MQTT server. Check your connection and make sure there is nothing blocking the connection such as a firewall or content blocker. Some users have reported problems with [pihole](https://pi-hole.net/). Adding an exception should solve the problem.

* **Screen OLED inverted**
The OLEd display changes depending on the hour: during the day is white and during the night is black. This change
protects the OLED by changing the lit pixels from time to time, otherwise some pixels may burn out sooner.

* **What does CRC error mean and why doesn't it appear as a received packet**
The Cyclic Redundancy Check (CRC) verifies the integrity of the received packet. Some packets with CRC errors are expected. The LoRa demodulation can find packets despite a lot of noise. Some false positive results are expected and in some receiver configuration we may receive a lot. The CRC check is a filter for these packets, but they are not necessarily an indicator of bad hardware.

* **Why can't I access to the MQTT server as I did before?**
Check the [Programmatic API](https://github.com/G4lile0/tinyGS/wiki/Programmatic-API) for a more in depth explanation.




