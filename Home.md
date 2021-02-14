  tinyGS Open Ground Station Network
TinyGS is an open network of Ground Stations distributed around the world to receive and operate LoRa satellites and weather probes, using cheap and versatile modules.

This project is based on ESP32 boards and currently it is compatible with sx126x and sx127x but we plan to support more in the future. You can build your own board using one of these modules but most of us use a development board like the ones listed below.

# Supported boards
* **Heltec WiFi LoRa 32 V1** 
* **Heltec WiFi LoRa 32 V2** 
* **TTGO LoRa32 V1** 
* **TTGO LoRa32 V2** 
* **T-BEAM + OLED** 
* **ESP32 dev board + SX126X with crystal (Custom build, OLED optional)**
* **ESP32 dev board + SX126X with TCXO (Custom build, OLED optional)**
* **ESP32 dev board + SX127X (Custom build, OLED optional)**
* **TTGO LoRa32 V2 (Manualy swaped SX1267 to SX1278)**

**Important** verify that the board that you chosse support the band of the satellites that you want to receive. 

## Supported modules
* sx126x
* sx127x


Initially it was developed as a "weekend" project for the FossaSAT-1 LoRa satellite. We are passionate about space and created this project to be able to track and use the satellites to learn an experiment about …- Currently the network is open to any LoRa satellite and we also support other flying objects that have a compatible radio modulation with our hardware such as FSK, GFSK, LR-FHSS …..

It allows the operator of the Satellites/Probes to receive and operate their devices across the globe rather than just only when they fly over their location .

We are using Telegram as the mean of communication for the project, there are also two channels where you can suscribe and be updated automátically whenever a new packet is received by the network from the Satellite.

* **Main community chat:** https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q
* **Data channel (station status and received packets):** https://t.me/FOSSASAT_DATA
* **Test channel (simulator packets received by test groundstations):** https://t.me/FOSSASAT_TEST

## **Milestones:**

* Nov 28, 2019  ESP32-OLED-Fossa-GroundStation    project born.
* Dec  6, 2019   FossaSAT-1 deployed with an Electron rocket by Rocket Lab.
* Dec 10,2019     YL3CT’s GS receive the fist LoRa packet from FossaSAT-1
* Sep 28,2020    6U Norby LoRa satellite is deployed with a Soyuz-2-1b launcher
* Oct 11, 2020    KA9ETC’s GS receive the first LoRa packet from Norby
* Jan 24, 2021    3x V-R3x sat deployed with a Falcon-9
* Jan 25, 2021    KA9ETC’S GS receive the first LoRa packet from V-R3x
* Feb 14, 2021    New name and web tinyGS.com with a new Beta firmware.

## **Upcoming LoRa Satellites**

* Feb 28,2021    SD SAT will launch by ISRO PSLV rocket 
* Mar 15, 2021    FossaSat 1B, FossaSat 2 & NPS-CENETIX-Orbital 1 with Firefly
