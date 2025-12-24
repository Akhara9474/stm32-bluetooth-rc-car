# stm32-bluetooth-rc-car
Bluetooth-controlled RC car using STM32 and L298N

# STM32 Bluetooth RC Car (HC-05 + L298N)

## Overview
A Bluetooth-controlled RC car built using the STM32F407 and an L298N motor driver.  
Commands sent from a phone (Android only as not compatible with IOS) over Bluetooth (HC-05) control forward, backward, stop, and turning behavior.

## Features
- PWM motor speed control (TIM1)
- Direction control using GPIO (L298N IN pins)
- Bluetooth UART command control (HC-05)
- Battery-powered standalone operation (Used x4 AA Batteries)

## Hardware
- STM32F407 (Discovery or custom setup)
- L298N motor driver
- DC motors
- HC-05 Bluetooth module
- Battery pack (AA or equivalent)

## Folder Structure
- STM32CubeIDE project files (Core, Drivers, .ioc)
- wiring diagrams, photos, troubleshooting notes

## Wiring Summary (example)
- ENA → TIM1 CH1 (PWM)
- ENB → TIM1 CH2 (PWM)
- IN1/IN2/IN3/IN4 → GPIO outputs
- HC-05 TX → STM32 RX
- HC-05 RX ← STM32 TX (use voltage divider)

See full details in wiring files

## How to Build & Flash
1. Open `bt_rc_car.ioc` in STM32CubeIDE
2. Generate code (if needed)
3. Build project

