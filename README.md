
## 🌳 MQTT Topic Tree

mqtt-demo-a/
├── sensors (Published by ESP32)
│ ├── ldr
│ ├── temperature
│ └── timestamp
│
├── led1 (Subscribed by ESP32 → Controls Red LED)
└── led2 (Subscribed by ESP32 → Controls Green LED)
