# Voron 2.4 250mm Duet2Wifi + Duex5 Configuration

![Voron2.4](https://img.shields.io/badge/Voron2.4-3D%20Printer-blue)
![Duet2Wifi](https://img.shields.io/badge/Duet2Wifi-Board-blue)
![Klipper](https://img.shields.io/badge/Klipper-Firmware-green)

Welcome to the Voron 2.4 250mm Duet2Wifi + Duex5 Configuration repository! This repository contains the configuration files necessary for setting up and running a Voron 2.4 3D printer with a 250mm build volume using a Duet2Wifi and Duex5 board with Klipper firmware.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Voron 2.4 is a high-performance, CoreXY 3D printer designed for speed and precision. The Duet2Wifi and Duex5 boards provide a robust and flexible control system, while Klipper firmware enhances performance and customization capabilities.

This repository provides the configuration files to get your Voron 2.4 250mm up and running with a Duet2Wifi and Duex5 board using Klipper firmware. **Note:** This setup requires wiping the Duet board and using a Raspberry Pi as a host.

## Features

- Comprehensive configuration files for the Voron 2.4 with Duet2Wifi and Duex5.
- Optimized settings for high-speed and high-precision 3D printing.
- Easy-to-follow instructions for setup and calibration.
- Integration with Klipper firmware for enhanced performance.

## Getting Started

To get started with this configuration, you'll need the following:

- A Voron 2.4 3D printer with a 250mm build volume.
- A Duet2Wifi and Duex5 board.
- A Raspberry Pi to act as the host.
- Access to this repository.

### Prerequisites

Make sure you have the following software and tools installed:

- [Klipper Firmware](https://www.klipper3d.org/)
- [Duet Web Control](https://duet3d.dozuki.com/Wiki/Duet_Web_Control)

### Installation

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/Turbotorte2072/Voron_2.4_250_Duet_Klipper_Config.git
    ```

2. Follow the setup instructions in the [Klipper documentation](https://www.klipper3d.org/Installation.html) to install Klipper firmware on your Duet2Wifi and Duex5 board.

3. Wipe the existing firmware from your Duet2Wifi and Duex5 board. Refer to the [Duet documentation](https://duet3d.dozuki.com/Wiki/Erase_Flash) for instructions on erasing the firmware.

4. Install Klipper firmware on the Duet2Wifi and Duex5 board using the instructions from the [Klipper documentation](https://www.klipper3d.org/Duet.html).

5. Set up a Raspberry Pi to act as the host for Klipper. Follow the [Klipper installation guide](https://www.klipper3d.org/RPi_microcontroller.html) for setting up the Raspberry Pi.

6. Copy the configuration files from this repository to the appropriate directories on your Duet2Wifi and Duex5 board.

## Configuration

The configuration files are located in the `config` directory. These files include settings for:

- Printer dimensions and kinematics.
- Endstops and probes.
- Heaters and temperature sensors.
- Motors and movement.

You may need to adjust some settings to match your specific build and preferences. Refer to the comments within the configuration files for guidance.

## Usage

Once the configuration files are loaded, you can control your Voron 2.4 using the Klipper firmware and Duet Web Control interface. Here are some useful commands and tips:

- Home the printer using the `Home All` button.
- Preheat the bed and hotend using the `Preheat` buttons.
- Load and start a print using the `Print` interface.

For detailed usage instructions, refer to the [Klipper documentation](https://www.klipper3d.org/) and [Duet Web Control documentation](https://duet3d.dozuki.com/Wiki/Duet_Web_Control).

## Contributing

We welcome contributions from the community! If you have any improvements or suggestions, please open an issue or submit a pull request.

### How to Contribute

1. Fork this repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes and commit them with a descriptive message.
4. Push your changes to your fork.
5. Open a pull request to the `main` branch of this repository.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Thank you for using the Voron 2.4 Duet2Wifi + Duex5 Configuration! Happy printing!
