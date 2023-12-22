# How to build your own software from source

This guide will focus on the process for Windows Users. If MacOS/Linux will follow you will find them in there section:

## 📋 <a name="table">Table of Contents</a>

1. 💻 [Windows](#windows)
2. 🍏 [MacOS](#mac)
3. 🐧 [Linux](#linux)

## Requirements

- ESP IDF
- Espressif Tool VSCode
- This firmware is designed to run a Bitaxe v2+

## <a name="windows"> 💻 Windows

### Installation

- You need to install the Espressif tool from [here](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/windows-setup.html).
  On this page you will find a Get Started guide for installing this onto your machine.

      -   After you have installed the espressif tool onto your machine you need to install Visual Studio Code, link [here](https://code.visualstudio.com/).

          -   The next step is to install the `Espressif IDF` Extention in VSCode
          -   on the left sidebar click on the Extensions Tab and search for Espressif IDF and install the latest version

### Clone repository

Clone the [ESP-Miner](https://github.com/skot/ESP-Miner) repository and open it in VSCode.

### Configuration

After you have installed everything we need to configure the Espressif Tool.

View --> ESP-IDF: Device Configuration --> Device Target --> ESP-Miner --> esp32s3 --> ESP-S3 via USB Bridge

![configure-1](/pictures/1397/configure-1.gif)

### Build

Now we need to open an ESP-IDF terminal and cd into the `/main/http_server/axe-os/` folder and build the WebUI first and then we can build the firmware.
use

```linux
nmp run build
```

after that use this command:

```linux
idf.py build
```

![terminal](/pictures/1397/terminal.gif)

![terminal2](/pictures/1397/terminal1.gif)

The `idf.py` command needs to be executed in the ESP-Miner home directory so keep in mind to cd back into it after you build the WebUI.

After that you will find a `build` directory and in there you will find the `www.bin`and the `esp-miner.bin` files. These can be used to upload to your Bitaxe.

## <a name="mac"> 🍏 MacOS

## <a name="linux"> 🐧 Linux
