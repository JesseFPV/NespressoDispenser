# NespressoDispenser
Automatic Nespresso capsule dispenser system.

![bootimg2](https://user-images.githubusercontent.com/42770753/188196895-1454b54d-5c89-4117-9662-c9a8d76a90eb.png)


## About
This project is a DIY project to use at home and in no way affiliated with Nespresso or any other coffee brand. The project is modular what means you can use any desired quantity of slots (2+), as long as you have enough available GPIO pins.

## Versions
There are 2 versions to build:
- Simple Version (Dispenser + Webpage) (Raspberry Pico, Raspberry Pi Zero/3/3B/4B)
- Premium Version (Dispenser with Touchsceen and Barcode Scanner + Webpage) (Raspberry Pi 3B, Raspberry Pi 4B)

## Collaborate & Discuss on Discord
I've opened a Discord server (still very empty) to be able to help & discuss if others want to build or improve the system.
https://discord.gg/HcnCwzZeMX


## Main System Setup
The whole combined system excist of multiple sub-systems.
* Tablet User Interface (HTML, CSS, JS)
* Dispenser User Interace (HTML, CSS, JS) for Premium version with Touchscreen.
* PHP API Endpoint
* MQTT Broker
* Coffee Dispenser Hardware



### Tablet User Interface
TBA


### Dispenser User Interface
TBA


### PHP API Endpoint
TBA


### MQTT Broker
An MQTT connection is used to send dispense 'actions' to the Nespresso Capsule Dispenser (hardware). For the use of this setup I'm using the free cloud broker HiveMQ (https://hivemq.com/). However it is also possible to host your own MQTT broker. For most users the free plan of HiveMQ would be more than enough. 
