# STM32 ADC + Timer + DMA + UART Project

## Overview
This project demonstrates the use of **Timer-triggered ADC conversion with DMA** on an **STM32F103C8 (Black Pill)** microcontroller using **STM32CubeIDE**.

---

## Objectives
The project implements the following:

1. A 100 Hz Timer (TIM2)
2. ADC conversion triggered by timer overflow
3. DMA used to transfer ADC data to memory
4. ADC conversion complete interrupt
5. UART support included for optional debugging/output

---

## Project Architecture
- TIM2 generates periodic update events (100 Hz)
- ADC1 is configured to start conversion on TIM2 trigger
- DMA transfers ADC result directly to memory
- HAL callback is used to process conversion completion
- No continuous polling is used in the main loop

---

## Code Structure

Core/
├── Src/
│ ├── main.c → Application entry point
│ ├── adc.c → ADC configuration
│ ├── tim.c → Timer (TIM2) configuration
│ ├── dma.c → DMA configuration
│ └── usart.c → UART configuration
└── Inc/
└── Header files

Drivers/
└── STM32 HAL and CMSIS drivers

STM32_ADC_project.ioc → CubeMX configuration file

---

## Tools Used
- STM32CubeIDE
- STM32CubeMX
- HAL Library

---

## Target Hardware
- MCU: STM32F103C8
- Board: Black Pill

---

## Notes
- Code builds successfully.
- This project is tested at compilation level.
- Hardware verification can be done using a blackpill board and USB-UART converter.
---

## Author
Kumutha G


