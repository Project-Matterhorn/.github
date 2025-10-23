## ℹ️ Intro

### What is Project Matterhorn?
Project Matterhorn is a personal project initiated by Zerrium to address off-grid communication problem when hiking/mountaineering utilizing LoRa (long range radio) and GPS combo to track location and chat to each other with basic encryption for privacy and security.<br><br>

### We already have Walkie-Talkie, what makes this one different compared to it?

| **Aspect** | **Walkie-Talkie** | **Project Matterhorn** |
| :--- | :--- | :--- |
| Communication | Voice chat | Text-encrypted chat |
| GPS Location sharing | :x: | :white_check_mark: |
| Privacy | Anyone with the same<br>frequency can eavesdrop | Encrypted with basic cryptography |
| Reliability | Uncertain | Guaranteed by CRC[^1] and FEC[^2] mechanism<br>so it is more interference resistant |
| Range | Similar | Similar or slighly better |

<br>

### Why is this project called Matterhorn?
It is just a project codename taken from a mountain of Alps located in between the border of Switzerland and Italy. The name Matterhorn derives from the German words Matte ("meadow") and Horn ("horn"), and is often translated as "the peak of the meadows".[^3] This mountain also appears on the Toblerone packaging.[^4]<br><br>

### Plan
This project will be split into 2 parts: hardware side and software side.<br>
The hardware side will use:
- ESP32 S3
- LoRa SX1262
- GPS Ublox M10
- Micro SD card for storing GPX[^5] log and A-GNSS[^6] (AssistNow Ublox) data
- Barometer BMP280
- Thermometer AHT20
- Nokia 1202 LCD
- Accelerometer ADXL345 for fall/crash detection]
<br>

The software side will use PWA[^7] which works offline and use web socket to the ESP32 (with hotspot/AP mode) for the communication. In the PWA, you can send/read chats, see visual map location of other friends and import offline map.<br><br>

## 🎯 Milestones
- [x] ReactJS PWA (23 Sep 2025)
- [x] Offline map import to PWA (23 Sep 2025)
- [ ] Web front-end finishing
- [x] Initial LoRa range test (19 Oct 2025)
- [ ] Finalizing LoRa parameter settings
- [ ] GPS implementation with A-GNSS and GPX logging
- [ ] Barometer implementation for altimeter
- [ ] Fall/crash detection using accelerometer
- [ ] PCB design
- [ ] 3D rainproof enclosure design
- [ ] Web socket integration between ESP32 and PWA
- [ ] Final assembly
- [ ] Battery life test
- [ ] Final test in a real mountain
<br><br>

## ✔️ Acknowledgement
I would like to thank everyone who supports, donates and/or contribute to this experimental project. Hopefully in 6-12 months we can use this device to actually aid communication and enhance hiking experience together.<br><br><br>

[^1]: CRC: Cyclic Redundancy Check, [reference](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)
[^2]: FEC: Forward Error Correction, [reference](https://en.wikipedia.org/wiki/Error_correction_code)
[^3]: Reference https://en.wikipedia.org/wiki/Matterhorn
[^4]: Reference https://www.matterhornchalets.com/2017/08/01/15-facts-matterhorn/
[^5]: GPX: GPS Exhange Format. A file format to store GPS points, [reference](https://en.wikipedia.org/wiki/GPS_Exchange_Format)
[^6]: A-GNSS: Assisted Global Navigation Satellite System, [reference](https://en.wikipedia.org/wiki/Assisted_GNSS)
[^7]: PWA: Progressive Web App, [reference](https://en.wikipedia.org/wiki/Progressive_web_app)
