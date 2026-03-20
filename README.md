# STM32 GPIO Control via Registers - Project Overview

This is a bare-metal GPIO control project for STM32 microcontrollers that works directly with hardware registers instead of using high-level abstraction libraries (HAL or SPL).

## Table of Contents

1. [Core Objectives](#core-objectives)
2. [Main Features](#main-features)
3. [Hardware Used](#hardware-used)
4. [Project Structure](#project-structure)
5. [Getting Started](#getting-started)
6. [Contributing](#contributing)

---

## 1. Core Objectives

- **Develop deep understanding** of STM32 hardware architecture
- **Write optimized, low-level code** by manipulating registers directly
- **Master bare-metal programming** techniques for embedded systems

---

## 2. Main Features

### 2.1 Clock Configuration
Configure peripheral clocks using **RCC (Reset and Clock Control)** registers for precise control over system and peripheral clock signals.

### 2.2 GPIO Mode Setup
Set pin modes **(Input/Output/Alternate Function)** via:
- **MODER** registers (for STM32F4, STM32L1, and newer variants)
- **CRL/CRH** registers (for older STM32F1 variants like STM32F103)

### 2.3 GPIO Output Control
Drive pins High/Low using:
- **ODR (Output Data Register)** - standard control method
- **BSRR (Bit Set/Reset Register)** - for efficient atomic operations

### 2.4 LED Blinking Effects
Implement basic delay loops to create visible LED on/off patterns for system verification and debugging.

---

## 3. Hardware Used

| Component | Specification |
|-----------|---------------|
| **Microcontroller** | STM32F103C8T6 (Blue Pill board) or equivalent |
| **Programmer** | ST-Link V2 |
| **Peripheral** | Built-in LED on pin **PC13** |

---

## 4. Project Structure

```
STM32/
├── README.md                 # Project documentation
├── src/                      # Source code directory
│   └── main.c               # Main application code
├── inc/                      # Header files
│   └── stm32f103.h          # STM32F103 definitions
└── Makefile                  # Build configuration
```

---

## 5. Getting Started

### 5.1 Prerequisites

- **ARM GCC Toolchain** (arm-none-eabi-gcc)
- **ST-Link Utility** or OpenOCD
- **Text Editor or IDE** (VS Code, STM32CubeIDE, etc.)

### 5.2 Building the Project

```bash
# Clone the repository
git clone https://github.com/PhamTien102/STM32.git
cd STM32

# Build the project
make all

# Flash to device
make flash
```

### 5.3 Verification

1. Connect the ST-Link V2 programmer to your STM32 board
2. Upload the firmware using the flash command above
3. Observe the LED on PC13 blinking at regular intervals

---

## 6. Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

**Last Updated:** March 20, 2026

For questions or issues, please open a GitHub Issue in this repository.