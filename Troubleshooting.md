* **The config panel asks for user and password!!**
The user is always `admin` and the password is the password you configured during the setup process on the config panel itself. Read more on the [Ground Station configuraton page](https://github.com/G4lile0/ESP32-OLED-Fossa-GroundStation/wiki/Ground-Station-configuration).

* **I don't remember the password of the config panel!!**
Don't worry, you can reset to default parameters though the serial monitor, hitting key `e` on the keyboard or pushing and holding during 5 seconds the user button of the board during the credits screen of the oled during booting. After this you will need to connect to the config AP and set all the parameters. Read more on the [Ground Station configuraton page](https://github.com/G4lile0/ESP32-OLED-Fossa-GroundStation/wiki/Ground-Station-configuration).

* **How can I get the user and password for the MQTT server?**
We use [Telegram](https://telegram.org/) as the main communication channel and also it works as an extension of the project though our bot. You can join our [Community Chat](https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q) and our bot will provide you with a fresh set of user and password just for you.

* **I'm new and I want to get in, what hardware should I buy?**
Welcome! First, make sure you read the [Status of the project section](https://github.com/G4lile0/ESP32-OLED-Fossa-GroundStation/wiki). As you might know now, there are two main types of lora chips SX127X and SX126X. The second ones (even if they have a smaller number) are the newest and the ones that work with FossaSat-1. They offer some advantages over the old ones but there is less support for them at the moment. There is currently no ESP32 development board sold with SX1268 from the factory so you have two options: Building yours or buying a development board (TTGO or Heltec) 433MHz and aim for the new satellites expected to be launched on March 2020.

* **I have a LoRa Board with frequency 868 or 915 MHz can I use it**
FossaSat-1 transmits on 436.7 Mhz so you need a 433MHz board to be able to communicate with it. Other frequencies wont make the firmware fail but you will probably not be able to receive anything from the satellite.