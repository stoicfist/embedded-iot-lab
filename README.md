# Embedded IoT Lab

A hands-on learning project for exploring embedded systems, electronics, microcontrollers, Linux, and IoT.

The goal of this repository is not only to build working projects, but to understand what happens at both the hardware and software level.
From electrical signals and microcontroller peripherals to network communication and Linux-based data processing.

## Goals

This project is used to learn and experiment with:

* Microcontroller programming in C/C++
* Basic electronics and circuit design
* GPIO, ADC, PWM, timers, and interrupts
* Sensors and other electronic components
* UART, I²C, and SPI
* Reading datasheets and schematics
* Communication between microcontrollers and Linux systems
* Network communication and IoT protocols such as MQTT
* Hardware and software debugging
* Data acquisition, storage, and visualization

Rust may be explored later as an additional language for embedded development.

## Hardware

The project currently uses: 

**Microcontroller:**  

<details>
<summary><strong>Arduino MKR WiFi 1010</strong></summary>

| Specification | Arduino MKR WiFi 1010 |
|---|---|
| Microcontroller | SAMD21 Cortex-M0+ |
| Architecture | ARM Cortex-M0+ |
| Clock | 48 MHz |
| Operating voltage | 3.3 V |
| Flash memory | 256 KB |
| SRAM | 32 KB |
| Wireless | Wi-Fi + Bluetooth |
| Wireless module | u-blox NINA-W102 |
| Interfaces | UART, I²C, SPI |
| Analog features | ADC + DAC |
| USB | USB device |

</details>

**Linux Host:**

The Linux system is used for firmware development, serial communication,
network services, data processing, storage, and debugging.

<details>
<summary><strong>Development system</strong></summary>

| Specification | Development System |
|---|---|
| Device | Dell Inspiron 16 Plus 7630 |
| Operating System | Gentoo Linux x86_64 |
| Kernel | Linux 6.12.31-gentoo |
| CPU | Intel Core i7-13700H |
| GPU | NVIDIA GeForce RTX 4060 Laptop GPU |
| Integrated GPU | Intel Iris Xe Graphics |
| Memory | 32 GB |
| Desktop Environment | KDE Plasma |
| Shell | Zsh |

</details>

**Additional hardware:** Sensors, LED/display modules, and other components will be documented as they are added.

The repository is intentionally not tied to a single microcontroller platform. Other boards and architectures may be added in the future.


## Project Direction

The long-term architecture is roughly:

```text
Sensors / Electronics
        │
        ▼
Microcontroller
        │
        ▼
Network / IoT
        │
        ▼
Linux System
        │
        ├── Data processing
        ├── Storage
        └── Visualization
```

Development will be incremental. Individual concepts will first be explored in small experiments before being combined into larger applications.

## Planned Experiments

Initial topics include:

* GPIO and basic circuits
* Analog measurements using the ADC
* PWM and timers
* Interrupt handling
* UART communication with Linux
* I²C and SPI peripherals
* Sensor integration
* MQTT communication
* LED matrix/display control
* Remote communication through a VPN

One planned experiment is a small messaging system where encoded messages can be transmitted to the microcontroller, decoded, and displayed on an LED matrix.

## Philosophy

This repository focuses on understanding rather than simply assembling libraries.

Whenever practical, experiments will investigate what abstractions such as Arduino libraries actually do underneath, including registers, protocols, timing, and electrical behavior.

The objective is to gradually move from high-level Arduino development toward a deeper understanding of embedded systems.
