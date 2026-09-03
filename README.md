# Renesas_MPU_EmbSW_Overall_Offer

## Overview

Renesas MPU Embedded Software distribution is a set of software components, system build and development tools created to ease the development to be done on top of Renesas RZ MPU devices.

Renesas MPU Embedded Software distribution includes:

- A Linux® distribution, running on the Arm® Cortex®-A processor(s): the **Renesas RZ Verified Linux Package (VLP)** and **RZ Linux BSP**, delivered through Yocto layers and CIP-based kernel/bootloader repositories.
- An **FSP package**, running on the Arm® Cortex®-M / Cortex-R real-time processor(s): the **Renesas RZ Flexible Software Package (FSP)**.

> [!IMPORTANT]
> The Renesas RZ MPU offer is published across **two GitHub organizations**:
> - [`github.com/renesas`](https://github.com/renesas) — the **RZ FSP** (Cortex-M/R side), shared with the RA MCU tooling.
> - [`github.com/renesas-rz`](https://github.com/renesas-rz) — the **RZ Linux/Yocto BSP** (Cortex-A side): Yocto layers, CIP kernel, U-Boot, TF-A, OP-TEE, AI SDK, HMI SDK, and AOSP.
>
> Unlike a single `oe-manifest` entry point, the RZ Linux BSP is assembled from the individual component repositories listed below. A curated index is maintained at the [Renesas RZ Software org profile](https://github.com/renesas-rz).

The **Renesas RZ Verified Linux Package (VLP)** is a Linux® distribution based on the OpenEmbedded/Yocto build framework, using a CIP (Civil Infrastructure Platform) SLTS kernel for up to 10-year maintenance. It includes the following collection of software components.

**RZ Linux BSP (OP-TEE secure OS, boot chain and Linux kernel):**

- The boot chain based on TF-A and U-Boot
- The OP-TEE secure OS running on the Cortex®-A in secure mode
- The Linux kernel (CIP/SLTS) running on the Cortex®-A in non-secure mode

**Application frameworks** such as the following Linux application frameworks (non-exhaustive list):

- Wayland-Weston as a display/graphic framework
- GStreamer as a multimedia framework
- Advanced Linux Sound Architecture (ALSA) libraries

The **Renesas RZ FSP** is a comprehensive set of embedded software libraries and drivers, delivered for the RZ real-time cores. As of RZ FSP v4.x, the previously separate RZ/A, RZ/G, RZ/N, RZ/T and RZ/V FSPs are unified into a single package.

- The CMSIS modules corresponding to the Arm® core implemented in the RZ product
- The **RZ FSP HAL drivers**: an abstraction driver layer, the API ensuring maximized portability across the RZ portfolio
- The BSP for each evaluation board provided by the RZ series
- A consistent set of middleware components such as RTOS, OpenAMP, ...
- A full set of software projects (examples, applications or demonstrations) for each board provided by the RZ series

## Description

This repo is a simple Readme describing all Renesas RZ MPU related GitHub projects, the open source offer for the Renesas RZ MPU products.

## Renesas RZ FSP packages

The RZ FSP unifies all RZ series into one package, with per-series folders (`rza/`, `rzg/`, `rzn/`, `rzt/`, `rzv/`) inside a single repository.

| Package | Description | Repository |
| :--- | :--- | :--- |
| RZ FSP | Unified Flexible Software Package for RZ/A, RZ/G, RZ/N, RZ/T, RZ/V | [Go to repository](https://github.com/renesas/rz-fsp) |
| RZ FSP — RZ/A | RZ/A series FSP source (Cortex-A real-time / bare-metal) | [Go to repository](https://github.com/renesas/rz-fsp/tree/master/rza/rz) |
| RZ FSP — RZ/G | RZ/G series FSP source (Cortex-M sub-core) | [Go to repository](https://github.com/renesas/rz-fsp/tree/master/rzg/rz) |
| RZ FSP — RZ/N | RZ/N series FSP source | [Go to repository](https://github.com/renesas/rz-fsp/tree/master/rzn/rz) |
| RZ FSP — RZ/T | RZ/T series FSP source | [Go to repository](https://github.com/renesas/rz-fsp/tree/master/rzt/rz) |
| RZ FSP — RZ/V | RZ/V series FSP source | [Go to repository](https://github.com/renesas/rz-fsp/tree/master/rzv/rz) |
| RZ FSP Examples | Example and application projects for the RZ MPU family | [Go to repository](https://github.com/renesas/rz-fsp-examples) |

## Renesas RZ Linux BSP packages

The RZ Linux BSP (Cortex-A side) is assembled from the following component repositories in the [`renesas-rz`](https://github.com/renesas-rz) organization.

| Package | Description | Repository |
| :--- | :--- | :--- |
| meta-renesas | Yocto layer for Renesas RZ products (BSP + distro, Scarthgap) | [Go to repository](https://github.com/renesas-rz/meta-renesas) |
| rz_linux-cip | RZ Linux kernel based on the CIP/SLTS long-term-support tree | [Go to repository](https://github.com/renesas-rz/rz_linux-cip) |
| renesas-u-boot-cip | U-Boot bootloader for RZ platforms | [Go to repository](https://github.com/renesas-rz/renesas-u-boot-cip) |
| rzg_trusted-firmware-a | Arm Trusted Firmware-A (TF-A) for RZ platforms | [Go to repository](https://github.com/renesas-rz/rzg_trusted-firmware-a) |
| rzg_optee-os | OP-TEE secure OS for RZ platforms | [Go to repository](https://github.com/renesas-rz/rzg_optee-os) |
| rzg_optee-ta_fwu | OP-TEE Trusted Application for secure firmware update | [Go to repository](https://github.com/renesas-rz/rzg_optee-ta_fwu) |
| rz_tool_flash_writer | Flash Writer tool for programming RZ boot media | [Go to repository](https://github.com/renesas-rz/rz_tool_flash_writer) |
| rz-community-bsp | Community BSP for RZ reference platforms using latest upstream software | [Go to repository](https://github.com/renesas-rz/rz-community-bsp) |
| meta-rz-demos | Yocto layer providing RZ demonstration images | [Go to repository](https://github.com/renesas-rz/meta-rz-demos) |
| local_manifests | repo manifests for assembling the RZ Linux/AOSP source trees | [Go to repository](https://github.com/renesas-rz/local_manifests) |

## Renesas RZ Multimedia and Graphics packages

Multimedia and graphics enablement layered on top of the RZ Linux BSP.

| Package | Description | Repository |
| :--- | :--- | :--- |
| gst-omx | GStreamer OpenMAX IL plugin for RZ hardware video codecs | [Go to repository](https://github.com/renesas-rz/gst-omx) |
| gst-plugins-bad | GStreamer bad-plugins set for RZ multimedia pipelines | [Go to repository](https://github.com/renesas-rz/gst-plugins-bad) |
| rzg_gstreamer_vspmfilter | GStreamer VSPM filter plugin (video signal processing) for RZ/G | [Go to repository](https://github.com/renesas-rz/rzg_gstreamer_vspmfilter) |
| rz-virtual-uart | SubCore-based virtual UART solution for Linux (up to 10 Mbps) | [Go to repository](https://github.com/renesas-rz/rz-virtual-uart) |

## Renesas RZ/V Vision AI packages

Vision-AI enablement for the RZ/V series, centered on the DRP-AI accelerator and the RUHMI (formerly DRP-AI TVM) toolchain.

| Package | Description | Repository |
| :--- | :--- | :--- |
| rzv_drp-ai_tvm | RUHMI — AI model optimization/deployment for RZ/V, powered by EdgeCortix® MERA™ | [Go to repository](https://github.com/renesas-rz/rzv_drp-ai_tvm) |
| rzv_ai_sdk | RZ/V AI Software Development Kit (Yocto Linux + DRP-AI + graphics) | [Go to repository](https://github.com/renesas-rz/rzv_ai_sdk) |
| rzv_sample_apps | Reference/sample applications for RZ/V (camera, encode, AI) | [Go to repository](https://github.com/renesas-rz/rzv_sample_apps) |
| rzv2n_drp-ai_driver | DRP-AI driver for RZ/V2N | [Go to repository](https://github.com/renesas-rz/rzv2n_drp-ai_driver) |
| rzv2n_opencv_accelerator | DRP-accelerated OpenCV for RZ/V2N | [Go to repository](https://github.com/renesas-rz/rzv2n_opencv_accelerator) |
| meta-renesas-ai | Yocto layer adding FOSS AI frameworks (ArmNN, TFLite, ONNX Runtime) to RZ/G, RZ/V | [Go to repository](https://github.com/renesas-rz/meta-renesas-ai) |
| ruhmi-framework-rzg | RUHMI AI model compiler workflow for RZ/G3E | [Go to repository](https://github.com/renesas/ruhmi-framework-rzg) |

## Renesas RZ/G HMI packages

| Package | Description | Repository |
| :--- | :--- | :--- |
| rzg_hmi_sdk | HMI SDK for RZ/G — GUI frameworks and sample applications (LVGL, Chromium) | [Go to repository](https://github.com/renesas-rz/rzg_hmi_sdk) |

## Renesas RZ Android (AOSP) packages

| Package | Description | Repository |
| :--- | :--- | :--- |
| rz_aosp | Renesas RZ Android Open Source Project (AOSP) BSP | [Go to repository](https://github.com/renesas-rz/rz_aosp) |
| rzv_aosp_ai_apps | AI applications for RZ/V2H on the AOSP software package | [Go to repository](https://github.com/renesas-rz/rzv_aosp_ai_apps) |

## Renesas RZ Documentation and Solutions

| Package | Description | Repository |
| :--- | :--- | :--- |
| rz_solution | Sources for the Renesas RZ Linux Solutions website (github.io) | [Go to repository](https://github.com/renesas-rz/rz_solution) |
| rz_linux_distros | Sources for the RZ Ubuntu/Debian distros website (github.io) | [Go to repository](https://github.com/renesas-rz/rz_linux_distros) |
| rz-ethos-u-docs | Documentation for the RZ Ethos-U (NPU) package | [Go to repository](https://github.com/renesas-rz/rz-ethos-u-docs) |

## Supported RZ MPU boards

The following evaluation boards are supported across the RZ Linux BSP (Yocto `meta-renesas`) and RZ FSP. MPU part numbers are shown where published.

| Series | Board | MPU | Domain |
| :--- | :--- | :--- | :--- |
| RZ/G | RZ/G2L SMARC EVK | R9A07G044L | Linux (VLP) + FSP |
| RZ/G | RZ/G2LC SMARC EVK | R9A07G044C | Linux (VLP) + FSP |
| RZ/G | RZ/G2UL SMARC EVK | R9A07G043U | Linux (VLP) + FSP |
| RZ/G | RZ/G3S SMARC EVK | R9A08G045 | Linux (VLP) + FSP |
| RZ/G | RZ/G3E EVK | R9A09G047E57 | Linux (VLP) + FSP |
| RZ/G | RZ/G3L SMARC EVK | R9A08G046 | Linux (VLP) + FSP |
| RZ/V | RZ/V2L SMARC EVK | R9A07G054L | Linux + AI SDK |
| RZ/V | RZ/V2H EVK | R9A09G057H | Linux + AI SDK + AOSP |
| RZ/V | RZ/V2N EVK / FPB-RZV2N | R9A09G056 | Linux + AI SDK |
| RZ/T | RZ/T2H EVK | R9A09G077 | Linux (VLP) + FSP |
| RZ/N | RZ/N2H EVK | R9A09G087 | Linux (VLP) + FSP |
| RZ/A | RZ/A3UL EVK | — | FSP |

## Communication and support

For communication and support, you can use:

- [Renesas Support Center](https://www.renesas.com/support) for any defect
- [Renesas Engineering Community — RZ forum](https://community.renesas.com/rz/)

## About

Renesas_MPU_EmbSW_Overall_Offer

Readme &nbsp;•&nbsp; Code of conduct &nbsp;•&nbsp; Security policy
