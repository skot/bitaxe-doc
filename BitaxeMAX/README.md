# BitaxeMax(1397)

The BitaxeMax which uses the ASIC BM1397 chip was the first working open source Bitcoin miner.

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. 🛠️ [Hardware](#hardware)
3. ⚙️ [Guide the BitaxeMAX](#guide)
4. 🔋 [Features](#features)
5. 🎯 [Goals](#goals)
6. 📝 [To-Do's](#todo)
7. 🖼️ [Pictures](#pictures)

---

## <a name="introduction"> What is this?

The Bitaxe Max is a groundbreaking open-source Bitcoin standalone miner, representing a significant leap in mining technology. At its core, it employs an ASIC 1397 chip, a specialized application-specific integrated circuit designed for optimal Bitcoin mining performance. Adding to its innovative features, the Bitaxe Max is equipped with an ESP32-S3, serving as the brain of the miner and facilitating seamless connectivity to Wi-Fi networks.

One of the key strengths of the Bitaxe Max lies in its impressive hashrate range, boasting speeds between 250-450 gigahashes per second (Gh/s) while just using up to 15 watts. This high level of computational power allows for efficient and competitive Bitcoin mining, contributing to the overall security and decentralization of the network.

With its open-source nature, the Bitaxe Max not only provides cutting-edge mining capabilities but also encourages transparency and collaboration within the cryptocurrency community. This unique combination of advanced hardware, open-source philosophy, and substantial hashrate positions the Bitaxe Max as a noteworthy player in the world of Bitcoin mining.

---

## <a name="hardware">🛠️ Hardware

The Bitaxe in general uses an <b>ESP32-S3-WROOM-1</b> to operate the whole device. On there is a specificaly written Software that serves as the Brain of this operation. It does the handleing of the job functions to the ASIC and it allows to connect to the Internet over Wi-Fi.

- The BM1397 is a undocumented SHA256 mining ASIC from Bitmain. It's mostly used in the Antminer S17 and T17
- Bitmain claims the BM1397 has 0.03J/GH efficiency
- The BM1397 is available (new) for around $20 each and (used) for around $6 ea in small quantities.
- Choose your BM1397 version: [Guide here](https://d-central.tech/bm1397-ad-ag-ah-ai-antminer-17-series-chip-replacement-guide/)
- The BM1397 has the same footprint as the BM1387, but a very different pinout.
  - It also has two "Modes" that change some of the signal pins around to make chaining easy
- The BM1397 is driven by an undocumented protocol over UART. Baudrate is 115200bps by default but can go up to 6Mbps in order to provide mining jobs quickly enough to the ASIC daisy-chain.

---

# <a name="guide">⚙️ Guide

The BitaxeMAX be either purchased as a fully functional standalone Bitcoin miner, or you can build your own with the following guides in [Assembly](assembly.md) and [Building](building.md).

## Building

1. Building and Assembliy

   - These two readme files will guide you throu the process of whats needed to build and order your own BitaxeMAX board.
     - [Assembly-readme](assembly.md)
     - [Building-readme](building.md)

2. Schematics
   - Futhermore for a more detailed view into the Schematics of the BitaxeMAX board you can view [BitaxeMaxSchematic](bitaxeMax_schematic.pdf).

---

## <a name="features">🔋 Features

- **ESP32-S3-WROOM-1** wifi microcontroller on board
- **TI TPS40305** buck regulator steps down the 5V input to power the BM1397
- **Maxim DS4432U+** current DAC digitally adjusts the BM1397 core voltage from 0.04V to 2.4V
- **TI INA260** power meter measures the input voltage and current of the miner
- **Microchip EMC2101** measures the BM1397 internal diode temperature. Also PWM controls the fan and monitors tach output.
- Two **sweet** RGB status LEDs

---

## Software

Every Bitaxe is controlled by the open source available [ESP-Miner](https://github.com/skot/ESP-Miner) software. It features a WebUi for user friendly usage and controlablility.

- [ESP-Miner](https://github.com/skot/ESP-Miner) firmware in progress.

---

## Building

- Check out [building.md](building.md) for PCB ordering tips
- Check out [assembly.md](assembly.md) for assembly tips

---

## <a name="goals">🎯 Goals

- [x] Standalone Miner
- [x] Reverse Engineering the Bitmain BM1397
- [ ] Tweak the J/GH efficiency and figure out how far we can go

---

## <a name="todo">📝 To-Do's

Any open issues will be listed here.

### <a name="pictures">🖼️ Pictures

![BM1397](/pictures/1397/BM1397.png)
![bitaxeMAX](/pictures/1397/render.png)
