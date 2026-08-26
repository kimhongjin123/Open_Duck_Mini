# Connector and GPIO map

Pin numbers below come from the KiCad schematic/netlist. Verify physical orientation from the footprint's pin-1 marker before connecting hardware.

## External connectors

| Ref | Board function / nearby silkscreen | Pin mapping |
| --- | --- | --- |
| J1 | SERVO_L | 1: GPIO12 / servo L signal; 2: +5 V; 3: GND |
| J2 | 5V VOUT | 1: +5 V; 2: GND |
| J3 | FOOT_L | 1: GND; 2: GPIO22 / foot L input |
| J4 | FOOT_R | 1: GND; 2: GPIO27 / foot R input |
| J5 | Raspberry Pi 40-pin header | See the GPIO table below |
| J6 | IMU | 1: GPIO3 / I2C SCL1; 2: GPIO2 / I2C SDA1; 3: GND; 4: +3.3 V |
| J7 | SERVO_R | 1: GPIO13 / servo R signal; 2: +5 V; 3: GND |
| J8 | UART | 1: GPIO15 / UART RX; 2: GPIO14 / UART TX; 3: GND |
| J9 | Nearby silkscreen: EYE_R | 1: through R3 (220 Ohm) to GPIO24 / LED_L; 2: GND |
| J10 | Nearby silkscreen: PRJ_LED | 1: through R4 (220 Ohm) to GPIO25 / LED_R; 2: GND |
| J11 | SPEAKER | 1: +5 V; 2: GND; 3: GPIO18 / I2S BCLK; 4: GPIO21 / I2S DOUT; 5: GPIO19 / I2S LRCLK |
| J12 | 3.3V VOUT | 1: +3.3 V; 2: GND |
| J13 | 5V VIN barrel jack | 1: switched 5 V input through SW1; 2: GND |
| J14 | Nearby silkscreen: EYE_L | 1: through R6 (220 Ohm) to GPIO23 / LED_PRJ; 2: GND |

> [!CAUTION]
> J9, J10, and J14 have a confirmed silkscreen-to-net mismatch in this revision. Electrically, J9 is LED_L, J10 is LED_R, and J14 is LED_PRJ. Use the electrical mapping above.

## Raspberry Pi header signals used

| Physical pin | Net / function |
| ---: | --- |
| 1 | +3.3 V |
| 2 | +5 V |
| 3 | GPIO2 / I2C SDA1 |
| 5 | GPIO3 / I2C SCL1 |
| 6 | GND |
| 8 | GPIO14 / UART TX |
| 9 | GND |
| 10 | GPIO15 / UART RX |
| 12 | GPIO18 / I2S BCLK |
| 13 | GPIO27 / foot R |
| 15 | GPIO22 / foot L |
| 16 | GPIO23 / projector LED |
| 18 | GPIO24 / left-eye LED |
| 22 | GPIO25 / right-eye LED |
| 32 | GPIO12 / servo L |
| 33 | GPIO13 / servo R |
| 35 | GPIO19 / I2S LRCLK |
| 40 | GPIO21 / I2S DOUT |

All other J5 positions are unconnected in the shield schematic.
