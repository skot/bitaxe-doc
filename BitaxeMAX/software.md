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

### Step 1. Installation

To compile using ESP-IDF, you need to get the following packages. The command to run depends on which distribution of Linux you are using:

Ubuntu and Debian:

```Linux
sudo apt-get install git wget flex bison gperf python3 python3-pip python3-venv cmake ninja-build ccache libffi-dev libssl-dev dfu-util libusb-1.0-0
```

CentOS 7 & 8:

```Linux
sudo yum -y update && sudo yum install git wget flex bison gperf python3 cmake ninja-build ccache dfu-util libusbx
```

Arch:

```Linux
sudo pacman -S --needed gcc git make flex bison gperf python cmake ninja ccache dfu-util libusb
```

### Step 2. Get ESP-IDF

To build applications for the ESP32, you need the software libraries provided by Espressif in [ESP-IDF repository](https://github.com/espressif/esp-idf).

To get ESP-IDF, navigate to your installation directory and clone the repository with `git clone`, following instructions below specific to your operating system.

Open Terminal, and run the following commands:

```Linux
mkdir -p ~/esp
cd ~/esp
git clone --recursive https://github.com/espressif/esp-idf.git
```

ESP-IDF is downloaded into `~/esp/esp-idf`.

### Step 3. Set up the Tools

Aside from the ESP-IDF, you also need to install the tools used by ESP-IDF, such as the compiler, debugger, Python packages, etc, for projects supporting ESP32.

```Linux
cd ~/esp/esp-idf
./install.sh esp32s3
```

### Step 4. Setup Environments Variables

The installed tools are not yet added to the PATH environment variable. To make the tools usable from the command line, some environment variables must be set. ESP-IDF provides another script which does that.

In the terminal where you are going to use ESP-IDF, run:

```linux
. $HOME/esp/esp-idf/export.sh
```

**Note the space between the leading dot and the path!**

If you plan to use esp-idf frequently, you can create an alias for executing `export.sh`:

1. Copy and paste the following command to your shell's profile (`.profile`, `.bashrc`, `.zprofile`, etc.)

```linux
alias get_idf='. $HOME/esp/esp-idf/export.sh'
```

2. Refresh the configuration by restarting the terminal session or by running `source [path to profile]`, for example, `source ~/.bashrc`.

Now you can run `get_idf` to set up or refresh the esp-idf environment in any terminal session.

### Clone repository

Clone the [ESP-Miner](https://github.com/skot/ESP-Miner) repository and open it in VSCode.
