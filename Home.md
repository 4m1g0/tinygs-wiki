# ESP32-OLED-Fossa-GroundStation for Platformio
The aim of this project is to create an open network of ground stations for the Fossa Satellites distributed all over the world and connected through Internet.

This project is based on ESP32 boards and is compatible with sx126x and sx127x you can build you own board using one of these modules but most of us use a development board like the ones listed in the Supported boards section.

The developers of this project have no relation with the Fossa team in charge of the mission, we are passionate about space and created this project to be able to track and use the satellites as well as supporting the mission.

## [IMPORTANT] Status of the project
Currently we are at an early stage of development (just a couple of weeks of work), the current version is functional but not fully stable and we are actively developing new changes so you will have to update the firmware quite regularly if you want to stay updated.

The first Fossa satellite, FossaSat-1 was launched on December 12, 2019 and it is still in evaluation stage by the Fossa team, so it is important **not to communicate to the satellity and only listen** until the Fossa team says otherwise. 

FossaSat-1 is currently in a healthy state and sending packets, however several issues were found and are being evaluated:
* Satellite antenna and solar panels might not be properly deployed. Received signals from the satellite were too weak compared with theoretical values and simulations which could indicate an improper deployment of the antenna or no deployment at all. The team has tried to command an emergency deployment using high gain antennas during several days with no success.  The dyneema wire holding the solar panels and the anntena is expected to degrade in the orbit atmosphere over the next weeks or months. However it will be highly unlikely to be able to communicate by then as it has been transmitting in short circuit for a long time. Due to this it is not possible to receive FossaSat-1 signals without huge antennas.
* It was discovered a misconfiguration on FossaSat-1 LoRa module. The syncWord parameter used is `0x0F0F` which is not documented and not compatible with sx127x receivers. This means that even with high gain antennas, **it is really difficult to communicate with FossaSat-1 with a sx127x modules** although not impossible as [this was already achieved](https://twitter.com/G4lile0/status/1204311425025486848) with antenna 4 x 23 el (DK7ZB) with tracking, 20 cable, preamp 20 dB, 2 way splitter and module RFM98.
* The satellite might be rotating. The satellite has a Passive Magnetic Stabilization (PMS) system and the Fossa team pointed out that it seems to be stabilizing gradually.

The Fossa team has announced that **two new satellites will be launched on March 2020 and those will be 100% compatible** with all the boards including sx127x, so at this moment the priority is keep improving the project, try to receive communications form FossaSat-1 with high gain antenas and be prepared for the next launch on March when all bords will be compatible. 

We are using Telegram as the mean of communication for the project, there are also two channels where you can suscribe and be updated automátically whenever a new packet is received by the network from the Satellite.
* **Main community chat:** https://t.me/joinchat/DmYSElZahiJGwHX6jCzB3Q
* **Data channel (station status and received packets):** https://t.me/FOSSASAT_DATA
* **Test channel (simulator packets received by test groundstations):** https://t.me/FOSSASAT_TEST

## Supported boards
* **Heltec WiFi LoRa 32 V1** (433MHz SX1278)
* **Heltec WiFi LoRa 32 V2** (433MHz SX1278) https://heltec.org/project/wifi-lora-32/
* **TTGO LoRa32 V1** (433MHz SX1278)
* **TTGO LoRa32 V2** (433MHz SX1278)
* **T-BEAM + OLED** (433MHz SX1278)
* **ESP32 dev board + SX126X with crystal (Custom build, OLED optional)**
* **ESP32 dev board + SX126X with TCXO (Custom build, OLED optional)**
* **ESP32 dev board + SX127X (Custom build, OLED optional)**
* **TTGO LoRa32 V2 (Manualy swaped SX1267 to SX1278)**

## Supported modules
* sx126x
* sx127x