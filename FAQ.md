* **The config panel asks for user and password!!**
The user is always `admin` and the password is the password you configured during the setup process on the config panel itself. Read more on the [Ground Station configuraton page](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).

* **I don't remember the password of the config panel!!**
 Don't worry, you can reset to default parameters though : 
    * the serial monitor, hitting key `e` on the keyboard 
    * pushing and holding during 5 seconds the user button of the board during the credits screen of the oled during booting. 
    * reseting the GS 10 times within 30 seconds 

    After this you will need to connect to the config AP and set all the parameters. Read more on the [Ground Station configuration page](https://github.com/G4lile0/tinyGS/wiki/Ground-Station-configuration).

* **How can I get the user and password for the MQTT server?**
We use [Telegram](https://telegram.org/) as the main communication channel and also it works as an extension of the project though our bot. You can join our [Community Chat](https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q) and our bot will provide you with a fresh set of user and password just for you.

* **I'm new and I want to get in, what hardware should I buy?**
Fist choose the satellites that you want to receive, we recommend 433Mhz because is the band with more supported satellites. But some satellites like V-R3x only work in 915Mhz band. There are two main types of lora chips SX127X and SX126X. 

* **I have a LoRa Board with frequency 433,868 or 915 MHz can I use it in a different band**
Other frequencies wont make the firmware fail but you will probably not be able to receive anything from the satellite, due the matching circuits.

* **MQTT connection failed with error: failed, rc=-2**
The ground station could not connect to the MQTT server, check your connection and make sure there is nothing blocking the connection such as a firewall or content blocker. It has been reported some problems with [pihole](https://pi-hole.net/). Adding an exception should solve the problem.

* **Screen OLED inverted**
It change depending of the hour, during the day is white and during the night is black, it's not only cosmetic is to protect the OLED burning by changing the lit pixels from time to time, if you don't do so, some pixels will wear out faster than others.

* **What mean a CRC error and why it doesn't appear as a received packet**
The Cyclic Redundancy Check (CRC) verifies the integrity of the received packet. Some packets with CRC errors are expected. The LoRa demodulation can find packets out of noise. Some false positive results are expected and in some receiver configuration we may receive a lot. The CRC check is a filter for these packets, but they are not necessarily an indicator of bad hardware.

* **Why I cannot cannot access to the MQTT server as I did before?**
Check the [Programmatic API](https://github.com/G4lile0/tinyGS/wiki/Programmatic-API) for a more in depth explanation.

* **Why my OLED Display is sometimes all white and sometimes black?**
This is a new feature to protect the OLED hardware. All oled displays suffer wearout with time so now the station uses a light style for day hours and a dark style for the night, this ensures that all the OLED pixels wear out at the same pace making it not noticeable. Also an option to lower the OLED brightness was added to the configuration dashboard.


