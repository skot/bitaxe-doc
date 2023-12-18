![Logo](/pictures/logo-no-background.svg)
[![](https://dcbadge.vercel.app/api/server/3E8ca2dkcC)](https://discord.gg/3E8ca2dkcC)

# Bitaxe Documentation

This Documentation will focus on document everything that is related with the Bitaxe project.

Contributing to this Github repository is highly anticipated and will be done via Github Pull request.
More on how to do that can be found [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

---

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [How to documentation](#guide)
3. 🔋 [Features](#features)
4. 🎯 [Goals](#goals)
5. 📝 [To-Do's](#todo)
6. 🤸 [Quick Start](#quick-start)
7. 🚀 [More](#more)

---

## <a name="introduction">🤖 Introduction

The Bitaxe is a groundbreaking open-source Bitcoin standalone miner, representing a significant leap in mining technology. At its core, it employs an ASIC chip, a specialized application-specific integrated circuit designed for optimal Bitcoin mining performance. Adding to its innovative features, the Bitaxe is equipped with an ESP32-S3, serving as the brain of the miner and facilitating seamless connectivity to Wi-Fi networks.

One of the key strengths of the Bitaxe lies in its impressive hashrate range, boasting speeds between 250-500 gigahashes per second (Gh/s) while just using up to 15 watts. This high level of computational power allows for efficient and competitive Bitcoin mining, contributing to the overall security and decentralization of the network.

With its open-source nature, the Bitaxe not only provides cutting-edge mining capabilities but also encourages transparency and collaboration within the cryptocurrency community. This unique combination of advanced hardware, open-source philosophy, and substantial hashrate positions the Bitaxe as a noteworthy player in the world of Bitcoin mining.

<a href="https://discord.com/invite/3E8ca2dkcC" target="_blank"><img src="https://github.com/sujatagunale/EasyRead/assets/151519281/618f4872-1e10-42da-8213-1d69e486d02e" /></a>

---

## <a name="guide">⚙️ How to guide through this documentation

This project is divided into three separate parts.
Each of these parts will have it's own `README.md`

To find yourself in the correct Documentation about a specific model you want to build or get to know more about take a look in the [BitaxeMAX (BM1397)](/BitaxeMAX/), [BitaxeUltra (BM1366)](/BitaxeUltra/) and [BitaxeHex](/BitaxeHEX/) section.

> The numbers behind the naming refers to the ASIC chips that's been used

---

## <a name="features">🔋 Features

- <b>ESP32-S3-WROOM-1</b> wifi microcontroller on board
- <b>Bitmain ASIC</b> application-specific integrated circuit
- <b>FOSS</b>

---

## <a name="goals">🎯 Goals

- <b>Standalone:</b> can mine directly to your pool over Wi-Fi. No external computer needed.
- <b>Embedded:</b> low cost, low maintenance, high availability, high reliability, low power consumption.
- <b>ASIC:</b> based on the very efficient BM1366 from Bitmain.
- <b>Open Source:</b> everything of this project is available on Github.

---

## <a name="todo">📝 To-Do's

- [ ] Hex
- [ ] 201+ TP reading's

---

## <a name="quick-start">🤸 Quick Start

The Bitaxe-instructions.pdf file contains a general instruction set.

[Setup Instruction Guide](/Bitaxe-Instructions.pdf)

---

## <a name="more">🚀 More

### 1. Software

- The [ESP-Miner](https://github.com/skot/ESP-Miner) firmware used for the BM1397-based bitaxe has been adapted for the BM1366 and the current main branch can support both.
- There is still work to be done on reverse engineering the BM1366 register map. If you can help, get in touch!

### 2. Hardware

- The [Bitaxe](https://github.com/skot/bitaxe) repository hosts all hardware requirements and manufacturing files to build your own Bitaxe

### 3.💸Vendors

- There are currently two official OSMU vendors:

  - [OSMU](https://opensourceminer.com)
  - [JABIT](https://www.jabitaxe.com)

- And 4 other selling Bitaxe aswell:
  - [D-Central](https://d-central.tech)
  - [RGZen](https://www.rgzen.com/index.php)
  - [Altair](https://altairtech.io/product/bitaxe/)
  - [BitcoinMerch](https://bitcoinmerch.com/de/products/bitcoin-merch%C2%AE-bitaxe-1366-solo-bitcoin-miner-up-to-500gh-s)
