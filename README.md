# STM32 PWM LED Brightness Control

Software PWM implementation on STM32F103C8T6 Blue Pill microcontroller for LED brightness control with smooth fading effects.

## 🎯 Project Overview

This project demonstrates software-based Pulse Width Modulation (PWM) to control LED brightness on the STM32F103C8T6 microcontroller. The onboard LED fades smoothly in and out, creating a breathing effect.

## 🔧 Hardware Components

- **STM32F103C8T6 Blue Pill** Development Board
- **ST-LINK V2** Programmer/Debugger
- **Onboard LED** on PC13 pin

## 💡 Features

- ✅ Software PWM implementation (no timer peripherals needed)
- ✅ Smooth LED fading effect (breathing pattern)
- ✅ Adjustable brightness levels (0-100%)
- ✅ Variable fade speed control
- ✅ Efficient duty cycle management

## 🛠️ Development Environment

- **IDE:** STM32CubeIDE
- **Programming Language:** Embedded C
- **HAL Library:** STM32 HAL
- **Programmer:** ST-LINK V2
- **Flash Tool:** STM32CubeProgrammer

## 📊 Technical Implementation

### PWM Concept

PWM controls brightness by rapidly switching the LED ON/OFF at different duty cycles:

- **10% duty cycle** → Dim (LED ON for 10% of time)
- **50% duty cycle** → Medium brightness
- **100% duty cycle** → Full brightness

### Code Logic

```c
// Fade IN: brightness increases from 0 to 100
for(int brightness = 0; brightness <= 100; brightness++) {
    // Turn LED ON for 'brightness' duration
    // Turn LED OFF for remaining duration
    // Repeat to create smooth visual effect
}

// Fade OUT: brightness decreases from 100 to 0
```

The human eye perceives rapid ON/OFF switching as varying brightness levels.

## 🚀 Getting Started

### Prerequisites

- STM32CubeIDE installed
- ST-LINK drivers installed
- STM32F103C8T6 Blue Pill board
- ST-LINK V2 programmer

### Build & Flash

1. Clone this repository
2. Open project in STM32CubeIDE
3. Build the project (`Ctrl+B`)
4. Connect ST-LINK to Blue Pill:
   - 3.3V → 3V3
   - GND → GND
   - SWDIO → SWIO
   - SWCLK → SWCLK
5. Flash using STM32CubeProgrammer or IDE
6. Watch the LED fade smoothly!

## 📸 Demo

The onboard LED (PC13) fades from OFF → BRIGHT → OFF in a continuous loop, creating a breathing effect.

## 📝 Key Learning Outcomes

This project demonstrates:
- ✅ GPIO control and manipulation
- ✅ Software PWM vs Hardware PWM concepts
- ✅ Duty cycle and frequency relationship
- ✅ STM32 HAL programming
- ✅ Embedded C optimization techniques

## 🔄 Future Enhancements

- [ ] Add hardware PWM using Timer peripherals
- [ ] Multiple LED control with different patterns
- [ ] User-configurable fade speed via UART
- [ ] RGB LED color mixing
- [ ] Button-controlled brightness levels

## 📧 Contact

**Gudla Srikanth**  
📧 srikanthsk02@gmail.com  
🔗 [GitHub](https://github.com/srikanthgudla-eng) | [LinkedIn](#)

---

**Status:** ✅ Working | **Last Updated:** May 2025
