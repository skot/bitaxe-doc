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

## <a name="introduction">🤖 What is this?

The Bitaxe Ultra is a groundbreaking open-source Bitcoin standalone miner, representing a significant leap in mining technology. At its core, it employs an ASIC BM1366 chip, a specialized application-specific integrated circuit designed for optimal Bitcoin mining performance. Adding to its innovative features, the Bitaxe M Ultra is equipped with an ESP32-S3, serving as the brain of the miner and facilitating seamless connectivity to Wi-Fi networks.

One of the key strengths of the Bitaxe Ultra lies in its impressive hashrate range, boasting speeds between 300-600 gigahashes per second (Gh/s) while just using up to 15 watts. This high level of computational power allows for efficient and competitive Bitcoin mining, especially compared to the previous version the BitaxeUltra, contributing to the overall security and decentralization of the network.

With its open-source nature, the Bitaxe Ultra not only provides cutting-edge mining capabilities but also encourages transparency and collaboration within the cryptocurrency community. This unique combination of advanced hardware, open-source philosophy, and substantial hashrate positions the Bitaxe Ultra as a noteworthy player in the world of Bitcoin mining.

## <a name="hardware">🛠️ Hardware

- [BM1366 from NBTC on AliExpress](https://www.aliexpress.us/item/3256804709142138.html). I got the "AG" variant. Not really sure what the difference is.
- [40x40mm heatsink and 5V fan](https://www.aliexpress.com/item/2251832861666365.html) from a random AliExpress seller. At least half of these arrived broken in some way. But they are cheap and the working ones do keep the BM1387's nice and cool when used with some thermal compound.
  - Swap this fan with the [Noctua NF-A4x10](https://noctua.at/en/products/fan/nf-a4x10-pwm) 5V 4-Pin fan for a much more pleasant experience.
- Supports 0.91" SSD1306-based I2C OLED Module. [Example Amazon seller](https://www.amazon.com/gp/product/B08ZY4YBHL)
- The BM1366 serial port is 1.8V. These pins are broken out, but the main idea is to communicate with the BM1366 from the ESP32
- Level shifters to interface the 1.8V BM1366 with the 3.3V ESP32. These pins are also broken out.
- [KiCad 7](https://www.kicad.org) design files
- All of the parts on the board are listed in the KiCad BOM

The BM1366 is a undocumented SHA256 mining ASIC from Bitmain. It's mostly used in the Antminer S19XP.
Bitmain claims the BM1366 has 0.021J/GH efficiency

The BM1366 has a different footprint and pinout from the BM1397 and BM1387 in previous bitaxe.
The BM1366 appears to roll more than just the nonce on the chip. This is great news, because it allows much longer serial chains of ASICs and new work doesn't need to be sent as often.

---

## <a name="guide">⚙️ Guide

The BitaxeUltra can be either purchased as a fully functional standalone Bitcoin miner, or you can build your own with the following guides in [Assembly](assembly.md) and [Building](building.md). Building this on your own will take much longer and requires a high skillset of SMD soldering and handling.

## Building

1. Building and Assembliy

   - These two readme files will guide you throu the process of whats needed to build and order your own BitaxeUltra board.
     - [Assembly-readme](assembly.md)
     - [Building-readme](building.md)
   - There are some Videos and Streams about how to Assembly a Bitaxe from scratch from some YouTubers such as [D-Central](https://www.youtube.com/@DCentralTech) and [WantClue](https://www.youtube.com/@WantClue)

2. Schematics

   - Futhermore for a more detailed view into the Schematics of the BitaxeUltra board you can view [BitaxeUltraSchematic](/BitaxeUltra/BitaxeUltra-schematic.pdf).

3. Manufacturing Files
   - In the [Manufacturing_Files_Folder](Manufacturing_Files) you will find all the necessary files to create your own PCB from Gerber files and the BOM(Build of Matierial) a list of all the components needed to build the BitaxeUltra

---

## Software

1. Building your Software

   - You can build your own binary files from the source code. For more details follow this [Build-Guide](/BitaxeMAX/software.md).

2. Using a prebuild

   - Every Bitaxe is controlled by the open source available [ESP-Miner](https://github.com/skot/ESP-Miner) software. It features a WebUi for user friendly usage and controlablility.
   - In this repository you will also find a [releases](https://github.com/skot/ESP-Miner/releases) page that will contain prebuild binary files to flash to your Bitaxe using the [Bitaxetool](https://github.com/johnny9/bitaxetool) created by [johnny9](https://github.com/johnny9).

3. Flashing Process
   - The [ESP-Miner](https://github.com/skot/ESP-Miner) Software can be flashed via a USB cable onto the Bitaxe. Therefore you need to follow the initial Guide in the repository.

## <a name="features">🔋 Features

This documentation features the following:

- An interactive build of material, to allow you to assemble the Bitaxe quicker. [iBOM](/BitaxeUltra/Manufacturing_Files/ibom.html)
- The Bitaxe Ultra features a BM1366 ASIC chip (usually the AG variant)

## <a name="goals">🎯 Goals

- [x] The most efficient open source miner 19J/TH
- [ ] Make the mining industry a bit more open source

## <a name="todo">📝 To-Do's

- [ ] TP Readings
- [ ] Freq / Voltage area

### <a name="pictures">🖼️ Pictures

![BitaxeUltra](/pictures/1366/201/IMG_5248.jpeg)
