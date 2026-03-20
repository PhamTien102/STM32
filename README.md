STM32 GPIO Control via Registers - Project Overview
This is a bare-metal GPIO control project for STM32 microcontrollers that works directly with hardware registers instead of using high-level abstraction libraries (HAL or SPL).

Core Objectives:
Develop deep understanding of STM32 hardware architecture
Write optimized, low-level code by manipulating registers directly
Main Features:
Clock Configuration - Configure peripheral clocks using RCC (Reset and Clock Control) registers

GPIO Mode Setup - Set pin modes (Input/Output/Alternate Function) via MODER registers (or CRL/CRH for older STM32 variants)

GPIO Output Control - Drive pins High/Low using ODR (Output Data Register) or BSRR (Bit Set/Reset Register) for efficient control

LED Blinking Effects - Implement basic delay loops to create visible LED on/off patterns

Hardware Used:
Microcontroller: STM32F103C8T6 (Blue Pill board) [or equivalent]
Programmer: ST-Link V2
Peripheral: Built-in LED on pin PC13
