# RZ_MPU_Overall_Offer

# Renesas_MPU_EmbSW_Overall_Offer

## Overview

Renesas MPU Embedded Software distribution is a set of software components, system build and development tools created to ease the development to be done on top of Renesas RZ MPU devices.

Renesas MPU Embedded Software distribution includes:

- A Linux® distribution, running on the Arm® Cortex®-A processor(s): the **Renesas RZ Verified Linux Package (VLP)**
- An **FSP / bare-metal package**, running on the Arm® Cortex®-M (or real-time) processor: the **Renesas RZ FSP package**

The **Renesas RZ Verified Linux Package (VLP)** is a Linux® distribution based on the OpenEmbedded build framework. It includes the following collection of software components.

**RZ VLP BSP (OP-TEE secure OS, boot chain and Linux kernel):**

- The boot chain based on TF-A and U-Boot
- The OP-TEE secure OS running on the Cortex®-A in secure mode
- The Linux kernel running on the Cortex®-A in non-secure mode

**Application frameworks** such as the following Linux application frameworks (non-exhaustive list):

- Wayland-Weston as a display/graphic framework
- GStreamer as a multimedia framework
- Advanced Linux Sound Architecture (ALSA) libraries

The **Renesas RZ FSP** is a comprehensive embedded software libraries and drivers, delivered for each RZ series.

- The CMSIS modules (core and device) corresponding to the Arm® core implemented in this RZ product
- The **RZ FSP HAL drivers**: an abstraction drivers layer, the API ensuring maximized portability across the RZ portfolio
- The BSP Drivers of each evaluation or demonstration board provided by this RZ series
- A consistent set of middleware components such as RTOS, OpenAMP, ...
- A full set of software projects (basic examples, applications or demonstrations) for each board provided by this RZ series

## Description

This repo is a simple Readme describing all Renesas RZ MPU related GitHub projects, the open source offer for the Renesas RZ MPU products.

## Renesas MPU Embedded Software packages

### RZ Verified Linux Packages

| OpenSTLinux Package | Description |
| :--- | :--- |
| oe-manifest | Renesas RZ MPU Embedded Software overall manifest |
| meta-renesas | Renesas RZ MPU OpenEmbedded/Yocto BSP layer |
| meta-rz-scripts | Renesas RZ MPU OpenEmbedded/Yocto front-end scripts |
| meta-renesas-rz | Renesas RZ MPU OpenEmbedded/Yocto frameworks layer (demonstrators, image examples, ...) |
| meta-rz-features | Renesas RZ MPU OpenEmbedded/Yocto BSP layer add-ons (Smart Configurator machine, ...) |
| linux | Renesas RZ MPU Linux kernel on `*-rz` branch |
| u-boot | Renesas RZ MPU U-Boot on `*-rz` branch |
| trusted-firmware-a | Renesas RZ MPU Arm Trusted Firmware (for Cortex®-A) on `*-rz` branch |
| optee_os | Renesas RZ MPU OP-TEE OS on `*-rz` branch |
| gpu-binaries | GPU binaries, GPU kernel driver source code |
| linux-examples | Some Linux examples |
| rz-linux-application | Renesas RZ MPU boards default applications |
| optee-rz-addons | Renesas RZ MPU features and add-ons around the OP-TEE ecosystem |
| dt-rz | Renesas RZ MPU embedded software device tree configurations |
| ddr-phy | Firmware for DDR PHY on RZ MPU |

### Other MPU Packages

| Package | Description |
| :--- | :--- |
| RZ_FSP_RZG | RZ/G Cube running in non-secure Cortex®-M context |
| cmsis-device-rzg | Provides the RZ FSP CMSIS Device MPU Component of the RZ/G series. |
| rzgxx-hal-driver | Provides the RZ FSP MPU Component "hal_driver" of the RZ/G series. |
| RZ_FSP_RZV | RZ/V Cube running in non-secure Cortex®-M context |
| cmsis-device-rzv | Provides the RZ FSP CMSIS Device MPU Component of the RZ/V series. |
| rzvxx-hal-driver | Provides the RZ FSP MPU Component "hal_driver" of the RZ/V series. |
| RZ_FSP_RZA | RZ/A firmware |
| cmsis-device-rza | Provides the RZ FSP CMSIS Device MPU Component of the RZ/A series. |
| rzaxx-hal-driver | Provides the RZ FSP MPU Component "hal_driver" of the RZ/A series. |
| trusted-firmware-m | RZ Trusted Firmware-M running in secure Cortex®-M context |
| tf-m-tests | Provides tests for trusted-firmware-m component |
| rz-low-power | Contains source code of RZ MPU Low-power firmware |
| SCP-firmware | Renesas RZ MPU SCP-firmware on `-rz` branch |
| OpenBMC | How to set up OpenBMC for Renesas RZ MPU |
| meta-rz-ota | Renesas RZ MPU Yocto layer to demonstrate how the secure firmware update is working in the RZ VLP. |

## Renesas MPU Tools packages

| RZ Package | Description |
| :--- | :--- |
| RZ-DDRFW-UTIL | Renesas RZ MPU firmware used to initialize DDR and perform DDR tests |
| RZ-PRGFW-UTIL | Renesas RZ MPU multiple applications to manage the One-Time Programmable (OTP) |
| rz-wrapper4dbg | Renesas RZ MPU tool that adds a debug wrapper to an RZ FSBL image |
| wiki-rz-addons | Renesas RZ MPU wiki content outside wiki |

## RZ MPU Expansion Packages

### RZ-LINUX Packages

| Package | Description |
| :--- | :--- |
| RZ-LINUX-AI | OE meta layer to install AI frameworks and tools for the Renesas RZ MPU |
| RZ-LINUX-RT | OE meta layer to get the RZ-LINUX-RT expansion package |
| RZ-LINUX-PREDMNT | OE meta layer to get the Renesas Predictive Maintenance Platform application |
| RZ-LINUX-GNSS1 | OE meta layer to get the RZ-LINUX-GNSS1 expansion package |
| RZ-LINUX-TSNSWCH | RZ MPU Expansion Package that targets the Time-Sensitive Networking (TSN) switch |
| RZ-LINUX-AZURE | RZ MPU RZ VLP Expansion Package that targets Microsoft Azure IoT Edge for RZ/G and RZ/V product microprocessors |
| RZ-LINUX-AWS | RZ MPU RZ VLP Expansion Package that targets Amazon Web Services® AWS IoT Greengrass™ V2 for RZ/G and RZ/V product microprocessors |
| RZ-LINUX-QT | RZ MPU RZ VLP Expansion Package that targets Qt based application and graphical user interface (GUI) development for the RZ series microprocessors |
| RZ-LINUX-ISP | Open-source software package providing ISP (Image Signal Processing) image quality software targeting the RZ series that embed an ISP camera pipeline |
| RZ-LINUX-IGTW1 | Linux-based expansion software package designed for industrial application development on Renesas RZ MPU |

### RZ FSP Packages

| Package | Description |
| :--- | :--- |
| rz-fsp-freertos-mpu | Full integration of FreeRTOS in the RZ FSP environment for the RZ MPU series |

## Communication and support

For communication and support, you can use:

- [Renesas Support Center](https://www.renesas.com/support) for any defect
- [Renesas Engineering Community](https://community.renesas.com/) — RZ MPU forum

## About

Renesas_MPU_EmbSW_Overall_Offer

Readme &nbsp;•&nbsp; Code of conduct &nbsp;•&nbsp; Security policy
