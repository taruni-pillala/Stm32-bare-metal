# STM32 Bare-Metal Projects

Bare-metal firmware for STM32F103C8T6 (ARM Cortex-M3) written 
in C using direct register access — no HAL, no libraries.

## Projects

### 1. LED Blink
Blinks onboard LED on PC13 using direct GPIO register access.
- Enables GPIOC clock via RCC_APB2ENR
- Configures PC13 as output via GPIOC_CRH
- Toggles GPIOC_ODR bit 13 with software delay

### 2. UART Hello World
Sends "Hello from STM32!" to laptop every second via UART1.
- Configures PA9 as UART TX alternate function
- Sets baud rate 9600 via USART1_BRR register
- Polls TXE flag before sending each character

## Hardware
- STM32F103C8T6 Blue Pill (ARM Cortex-M3, 72MHz)
- CH340 USB-UART converter
- Flashed via STM32CubeProgrammer

## Tools
- STM32CubeIDE + ARM GCC toolchain
- STM32CubeProgrammer (UART flashing)
- Tera Term (serial terminal)

## About
2nd year ECE student building embedded systems skills
from bare-metal fundamentals up.
