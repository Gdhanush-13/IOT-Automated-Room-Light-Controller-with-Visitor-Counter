# IoT Automated Room Light Controller with Visitor Counter

An Arduino (C++) IoT system that automatically controls room lighting based on occupancy and maintains a real-time visitor count using IR sensors.

## Overview

Two IR sensors placed at a doorway detect when people enter or exit. A counter tracks the number of occupants and automatically switches the light ON when anyone is present and OFF when the room is empty â€” saving energy without manual intervention.

## Features

- **Automatic Lighting** â€” Light ON when room is occupied, OFF when empty
- **Visitor Counter** â€” Real-time entry/exit tracking
- **Dual IR Detection** â€” Separate sensors for entry and exit
- **Serial Monitor** â€” Live count output at 9600 baud
- **Energy Efficient** â€” Zero manual switching required

## Hardware Components

| Component | Quantity |
|-----------|----------|
| Arduino Uno / Nano | 1 |
| IR Sensor Module | 2 |
| LED / Relay Module | 1 |
| Jumper Wires | Several |
| Breadboard | 1 |

## Pin Connections

| Component | Arduino Pin |
|-----------|-------------|
| IR Sensor 1 (Entry) | Digital 2 |
| IR Sensor 2 (Exit) | Digital 3 |
| LED / Relay | Digital 13 |

## How It Works

`
Person enters â†’ IR Sensor 1 triggers first â†’ count++
Person exits  â†’ IR Sensor 2 triggers first â†’ count--
count > 0     â†’ Light ON
count == 0    â†’ Light OFF
`

## Getting Started

### Prerequisites
- [Arduino IDE](https://www.arduino.cc/en/software) installed
- Arduino Uno/Nano board and the listed components

### Upload

`ash
git clone https://github.com/Gdhanush-13/IOT-Automated-Room-Light-Controller-with-Visitor-Counter.git
`

1. Open `Code.cpp` in Arduino IDE
2. Select your board and COM port under **Tools**
3. Click **Upload**
4. Open Serial Monitor at **9600 baud** to see the live count

## License

MIT â€” free to use and modify.