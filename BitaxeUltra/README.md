# BitaxeUltra

The Bitaxe Ultra is the currently most used model.

---

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. 🛠️ [Hardware](#hardware)
3. ⚙️ [Configure the BitaxeUltra](#guide)
4. 🔋 [Features](#features)
5. 🎯 [Goals](#goals)
6. 📝 [To-Do's](#todo)

---

## <a name="introduction"> What is this?

The Bitaxe Ultra is a groundbreaking open-source Bitcoin standalone miner, representing a significant leap in mining technology. At its core, it employs an ASIC BM1366 chip, a specialized application-specific integrated circuit designed for optimal Bitcoin mining performance. Adding to its innovative features, the Bitaxe M Ultra is equipped with an ESP32-S3, serving as the brain of the miner and facilitating seamless connectivity to Wi-Fi networks.

One of the key strengths of the Bitaxe Ultra lies in its impressive hashrate range, boasting speeds between 300-600 gigahashes per second (Gh/s) while just using up to 15 watts. This high level of computational power allows for efficient and competitive Bitcoin mining, especially compared to the previous version the BitaxeMAX, contributing to the overall security and decentralization of the network.

With its open-source nature, the Bitaxe Ultra not only provides cutting-edge mining capabilities but also encourages transparency and collaboration within the cryptocurrency community. This unique combination of advanced hardware, open-source philosophy, and substantial hashrate positions the Bitaxe Ultra as a noteworthy player in the world of Bitcoin mining.

## Hardware

- [BM1366 from NBTC on AliExpress](https://www.aliexpress.us/item/3256804709142138.html). I got the "AG" variant. Not really sure what the difference is.
- [40x40mm heatsink and 5V fan](https://www.aliexpress.com/item/2251832861666365.html) from a random AliExpress seller. At least half of these arrived broken in some way. But they are cheap and the working ones do keep the BM1387's nice and cool when used with some thermal compound.
  - Swap this fan with the [Noctua NF-A4x10](https://noctua.at/en/products/fan/nf-a4x10-pwm) 5V 4-Pin fan for a much more pleasant experience.
- Supports 0.91" SSD1306-based I2C OLED Module. [Example Amazon seller](https://www.amazon.com/gp/product/B08ZY4YBHL)
- The BM1366 serial port is 1.8V. These pins are broken out, but the main idea is to communicate with the BM1366 from the ESP32
- Level shifters to interface the 1.8V BM1366 with the 3.3V ESP32. These pins are also broken out.
- [KiCad 7](https://www.kicad.org) design files
- All of the parts on the board are listed in the KiCad BOM

---

# <a name="features">🔋 Features

ibom

![BitaxeUltra](/pictures/1366/201/IMG_5248.jpeg)
