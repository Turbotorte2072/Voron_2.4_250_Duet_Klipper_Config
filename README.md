# 🚀 Voron 2.4 250mm Duet2Wifi + Duex5 Configuration

![Voron2.4](https://img.shields.io/badge/Voron2.4-3D%20Printer-blue)
![Duet2Wifi](https://img.shields.io/badge/Duet2Wifi-Board-blue)
![Klipper](https://img.shields.io/badge/Klipper-Firmware-green)

Welcome to the Voron 2.4 250mm Duet2Wifi + Duex5 Configuration repository! This repository contains the configuration files necessary for setting up and running a Voron 2.4 3D printer with a 250mm build volume using a Duet2Wifi and Duex5 board with Klipper firmware.

## 📋 Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
- [Flashing Klipper on Duet2Wifi](#flashing-klipper-on-duet2wifi)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## 🔧 Introduction

The Voron 2.4 is a high-performance, CoreXY 3D printer designed for speed and precision. The Duet2Wifi and Duex5 boards provide a robust and flexible control system, while Klipper firmware enhances performance and customization capabilities.

This repository provides the configuration files to get your Voron 2.4 250mm up and running with a Duet2Wifi and Duex5 board using Klipper firmware. **Note:** This setup requires wiping the Duet board and using a Raspberry Pi as a host.

## 🌟 Features

- 📁 Comprehensive configuration files for the Voron 2.4 with Duet2Wifi and Duex5.
- ⚡ Optimized settings for high-speed and high-precision 3D printing.
- 🛠️ Easy-to-follow instructions for setup and calibration.
- 🚀 Integration with Klipper firmware for enhanced performance.

## 🚀 Getting Started

To get started with this configuration, you'll need the following:

- 🖨️ A Voron 2.4 3D printer with a 250mm build volume.
- 🖥️ A Duet2Wifi and Duex5 board.
- 🍓 A Raspberry Pi to act as the host.
- 📂 Access to this repository.

### 📋 Prerequisites

Make sure you have the following software and tools installed:

- [Klipper Firmware](https://www.klipper3d.org/)

## ⚙️ Flashing Klipper on Duet2Wifi

To flash Klipper firmware onto your Duet2Wifi board, follow these steps:

1. **Prepare the Raspberry Pi:**
   - Follow the [Klipper installation guide](https://www.klipper3d.org/RPi_microcontroller.html) to set up your Raspberry Pi.

2. **Install Klipper Firmware:**
   - Connect to your Raspberry Pi via SSH.
   - Run the following commands to install Klipper:

     ```bash
     git clone https://github.com/Klipper3d/klipper
     cd klipper
     make menuconfig
     ```

   - In the configuration menu, select the following options:
     - **Micro-controller Architecture:** `SAM3/SAM4 (Due and Duet)`
     - **Processor model:** `SAM4E8E (Duet WiFi/Eth)`
     - **Communication interface:** `USB (on USART0 PA11/PA10)`

   - Save and exit the configuration menu, then run:

     ```bash
     make
     ```

3. **Flash the Firmware:**
   - Connect the Duet2Wifi board to your Raspberry Pi using a USB cable.
   - Run the following command to flash the firmware:

     ```bash
     sudo service klipper stop
     make flash FLASH_DEVICE=/dev/serial/by-id/usb-bossa_*
     sudo service klipper start
     ```

4. **Configure Klipper:**
   - Copy the `printer.cfg` file from this repository to your Raspberry Pi:

     ```bash
     scp path/to/your/repo/config/printer.cfg pi@raspberrypi.local:~/printer.cfg
     ```

   - Edit the `printer.cfg` file to match your specific setup.

5. **Start Klipper:**
   - Restart the Klipper service:

     ```bash
     sudo service klipper restart
     ```

For detailed instructions, refer to the [Klipper documentation](https://www.klipper3d.org/).

## 🔧 Configuration

The configuration files are located in the `config` directory. These files include settings for:

- 📏 Printer dimensions and kinematics.
- 🔧 Endstops and probes.
- 🌡️ Heaters and temperature sensors.
- 🔄 Motors and movement.

You may need to adjust some settings to match your specific build and preferences. Refer to the comments within the configuration files for guidance.

## 📖 Usage

Once the configuration files are loaded, follow the official Voron documentation to complete the setup and calibration of your printer. Here are some useful links:

- [Voron Documentation](https://docs.vorondesign.com/)
- [Klipper Documentation](https://www.klipper3d.org/)

Following the guides provided in the documentation will help you achieve the best performance and reliability for your Voron 2.4 printer.

## 🤝 Contributing

We welcome contributions from the community! If you have any improvements or suggestions, please open an issue or submit a pull request.

### How to Contribute

1. 🍴 Fork this repository.
2. 🌿 Create a new branch for your feature or bugfix.
3. 📝 Make your changes and commit them with a descriptive message.
4. 🔄 Push your changes to your fork.
5. 📨 Open a pull request to the `main` branch of this repository.

## 📜 License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Thank you for using the Voron 2.4 Duet2Wifi + Duex5 Configuration! Happy printing! 🎉
