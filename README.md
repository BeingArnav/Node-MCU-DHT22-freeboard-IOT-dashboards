---
services: iot-hub
platforms: arduino
author: Arnav
---

# Node-MCU-DHT22-freeboard-IOT-dashboards
[![Build Status](https://learn.adafruit.com/tmp36-temperature-sensor/using-a-temp-sensor)]
(https://dweet.io/play/)

> This repo contains the source code to help you get familiar with Adafruit/Sparkfun IoT using the Adafruit IoT DHT22 ESP8266 Interference.

This repo contains an arduino application that runs on ESP8266 with a DHT22 temperature&humidity sensor, and then sends these data to your IoT hub/web-server. At the same time, this application receives Cloud-to-Device message from dweet.io, and uses Real Time web clouding on freeboard.io.

## Create your Cloud IoT hub
Follow [this page](https://freeboard.io/login) to login and register your device on freeboard.io

## Install board with your Arduino IDE
1. Start Arduino and open Preferences window.
2. Enter `http://arduino.esp8266.com/stable/package_esp8266com_index.json` into Additional Board Manager URLs field. You can add multiple URLs, separating them with commas.
3. Open Boards Manager from `Tools > Board` menu and install `esp8266 platform 2.2.0` or later
4. Select your ESP8266 board from `Tools > Board` menu after installation

## Install libraries
Install the following libraries from `Sketch -> Include library -> Manage libraries`

* `Adafruit Circuit Playground`
* `DHT sensor library`
* `Adafruit Unified Sensor`

## Connect your sensor with your board
### Connect with a physical DHT22 sensor
You can follow the image to connect your DHT22 with your feather HUZZAH ESP8266.

![DHT22](https://docs.microsoft.com/en-us/azure/iot-hub/media/iot-hub-arduino-huzzah-esp8266-get-started/15_connections_on_breadboard.png)


## Configure and run sample application
Upload the `DHT22_sensor_iot.ino` to your board.

### Input your credential information
After you successfully upload the code to your board. You will see some prompt, input your credential information according to the prompts.

### Send Cloud-to-Device command
You can send a C2D message to your device. You can see the device prints out the message and blinks once receiving the message.
