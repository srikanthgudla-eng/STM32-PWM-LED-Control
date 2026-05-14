# STM32 PWM LED Control

A simple project demonstrating software-based PWM on STM32F103C8T6 to control LED brightness.

## What This Does

The onboard LED on the Blue Pill board fades in and out smoothly (like a breathing effect). I implemented software PWM by rapidly toggling the GPIO pin at different duty cycles to create varying brightness levels.

## Components Used

- STM32F103C8T6 Blue Pill development board
- ST-LINK V2 for programming
- Onboard LED (PC13 pin)

## Key Features

- Software PWM implementation - no hardware timers needed
- Brightness control from 0% to 100%
- Smooth fading transition
- Adjustable fade speed

## Development Setup

I used STM32CubeIDE for this project along with the STM32 HAL library. Programming was done through ST-LINK V2 using STM32CubeProgrammer.

## How PWM Works Here

Instead of using hardware timer peripherals, I toggle the GPIO pin in software. By varying how long the LED stays ON vs OFF in each cycle, different brightness levels are achieved:

- 10% duty cycle = dim
- 50% duty cycle = medium  
- 100% duty cycle = full brightness

The code loops through brightness values from 0 to 100 and back down, creating the fade effect.

## What I Learned

- GPIO manipulation and timing
- Software vs hardware PWM tradeoffs
- STM32 HAL programming basics
- Embedded C optimization

## Future Ideas

- Add hardware PWM using timers for comparison
- Control multiple LEDs with different patterns
- Add button control for user interaction

---

**Gudla Srikanth**  
srikanthsk02@gmail.com
