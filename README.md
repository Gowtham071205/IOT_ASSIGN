# ESP32 MQTT Sensor Simulation (Wokwi + Mosquitto)

###  Project Overview
This project demonstrates how to use an **ESP32** board running **MicroPython** to publish sensor readings (LDR and Temperature) and receive control commands (LED ON/OFF) via the **MQTT protocol**.  
The simulation runs entirely in **Wokwi** and communicates with the public MQTT broker **test.mosquitto.org**.

---

##  Features
 Publishes sensor readings (Light & Temperature)  
 Receives LED control commands via MQTT  
 Uses public broker for easy testing  
 Works entirely in Wokwi simulation  
 Demonstrates bidirectional MQTT communication  

## 🌳 MQTT Topic Tree

mqtt-demo-a/
├── sensors               (Published by ESP32)
│   ├── ldr
│   ├── temperature
│   └── timestamp
│
├── led1                  (Subscribed by ESP32 → Controls Red LED)
└── led2                  (Subscribed by ESP32 → Controls Green LED)




###  1. Subscribe to all topics

    mosquitto_sub -h test.mosquitto.org -t "mqtt-demo-a/#"

2. Publish LED control commands

Turn Red LED ON

    mosquitto_pub -h test.mosquitto.org -t "mqtt-demo-a/led1" -m "on"


Turn Red LED OFF

    mosquitto_pub -h test.mosquitto.org -t "mqtt-demo-a/led1" -m "off"


Turn Green LED ON

    mosquitto_pub -h test.mosquitto.org -t "mqtt-demo-a/led2" -m "on"


Turn Green LED OFF

    mosquitto_pub -h test.mosquitto.org -t "mqtt-demo-a/led2" -m "off"
