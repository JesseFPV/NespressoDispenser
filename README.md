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
* [Tablet User Interface](/docs/tablet_ui.md) (HTML, CSS, JS)
* [Dispenser User Interace](/docs/dispenser_ui.md) (HTML, CSS, JS) for Premium version with Touchscreen.
* [Dispenser Controller](/docs/dispenser_controller.md) for listening to MQTT and activating GPIO -> Servos
* [PHP API Endpoint + MySQLi database](/docs/php_api.md)
* [MQTT Broker](/docs/mqtt_broker.md).
* [Hardware Setup](/docs/hardware.md)



#### Tablet User Interface
The Tablet User Interface (TUI) is the interface that will be used by the guests to select the coffee they want (mostly on tablets). The idea is to have a smooth experience where you can see all specs from the available coffee types and send an order to the dispenser.


#### Dispenser User Interface
The Dispenser User Interface (DUI) is the interface shown on the touchscreen on the dispenser itself. It has some quick tasks and less information than the TUI. However it shows an order list with current orders placed through the TUI that can be marked as 'done'. It also possible to add stock


#### PHP API Endpoint + MySQLi database
Just a small PHP file that acts as API endpoint for the MySQLi database connection.


#### MQTT Broker
An MQTT connection is used to send dispense 'actions' to the Nespresso Capsule Dispenser (hardware). For the use of this setup I'm using the free cloud broker HiveMQ (https://hivemq.com/). However it is also possible to host your own MQTT broker. For most users the free plan of HiveMQ would be more than enough. If you use the RPI3/4 you can also install a MQTT broker on the PI, however you need to run all external connection through your internal WiFi, if you want to access the system from outside your home network you have to forward some ports of your router.

More info about [MQTT Broker](/docs//mqtt_broker.md).



## Timeline
1. Sketching and Testing
2. Project Domain
3. Creating Github
4. Adding Github Resources
