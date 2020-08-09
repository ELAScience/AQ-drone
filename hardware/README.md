# Hardware Guide

This project makes use of several off-the-shelf parts, however, it requires a few that are custom-made via PCB fabrication and 3D Printing.

## Parts List

| Name                                                                      | Quantity | Cost (per unit, if applicable) | Supplier   | Notes                                                                                                                                        |
| ------------------------------------------------------------------------- | -------- | ------------------------------ | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Custom Made PCB                                                           | 1        | \$0.40                         |            | We used JLCPCB to manufacture 5 copies for \$2.00 + shipping                                                                                 |
| PCB Base Plate                                                            | 1        | \$20.00                        |            | Used to secure the PCB and sensors to the drone's mounting kit. We used our own printer but makexyz.com seems to be the most cost-efficient. |
| Stacking Headers for Feather - 12-pin and 16-pin female headers           | 3        | \$1.25                         | Adafruit   | Used to attach the FeatherWings to the Feather and the Feather to the PCB                                                                    |
| Adafruit Feather M4 Express - Featuring ATSAMD51 - ATSAMD51 Cortex M4     | 1        | \$22.95                        | Adafruit   |                                                                                                                                              |
| Adalogger FeatherWing - RTC + SD Add-on For All Feather Boards            | 1        | \$8.95                         | Adafruit   |                                                                                                                                              |
| Adafruit Ultimate GPS FeatherWing                                         | 1        | \$39.95                        | Adafruit   |                                                                                                                                              |
| GPS Antenna - External Active Antenna - 3-5V 28dB 5 Meter SMA             | 1        | \$14.95                        | Adafruit   |                                                                                                                                              |
| SMA to uFL/u.FL/IPX/IPEX RF Adapter Cable                                 | 1        | \$3.95                         | Adafruit   |                                                                                                                                              |
| CR1220 12mm Diameter - 3V Lithium Coin Cell Battery - CR1220              | 1        | \$0.95                         | Adafruit   | Backup battery for the GPS                                                                                                                   |
| ADS1115 16-Bit ADC - 4 Channel with Programmable Gain Amplifier           | 2        | \$14.95                        | Adafruit   |                                                                                                                                              |
| Adafruit BMP388 - Precision Barometric Pressure and Altimeter             | 1        | \$9.95                         | Adafruit   |                                                                                                                                              |
| Adafruit Sensirion SHT31-D - Temperature & Humidity Sensor                | 1        | \$13.95                        | Adafruit   |                                                                                                                                              |
| PM2.5 Air Quality Sensor and Breadboard Adapter Kit - PMS5003             | 1        | \$39.95                        | Adafruit   |                                                                                                                                              |
| Arduino Nano                                                              | 1        | \$9.00                         | Amazon     | Used to interface with the PMS5003                                                                                                           |
| 3.3V, 3.6A Step-Down Voltage Regulator D36V28F3                           | 1        | \$11.95                        | Pololu     |                                                                                                                                              |
| 5V, 3.2A Step-Down Voltage Regulator D36V28F5                             | 1        | \$11.95                        | Pololu     |                                                                                                                                              |
| AlphaSense 4-Way AFE with CO, O3, NO, and H2S                             | 1        | \$379.00                       | AlphaSense |                                                                                                                                              |
| DJI Matrice 600 Pro                                                       | 1        | \$5699.00                      | DJI        |                                                                                                                                              |
| DJI Matrice 600 Series Zenmuse X3/X5/XT/Z3 Series Gimbal Mounting Bracket | 1        | \$200.00                       | DJI        |                                                                                                                                              |
| DJI Zenmuse X3                                                            | 1        | -                              | DJI        | At the time of making this list, pricing information for this was unavailable.                                                               |
| DJI Matrice 600 Upper Expansion Bay Kit                                   | 1        | -                              | DJI        | At the time of making this list, pricing information for this was unavailable.                                                               |
| -                                                                         | -        | -                              | -          | -                                                                                                                                            |
| **Total**                                                                 |          | **\$6511.5**                   |            |                                                                                                                                              |

## Assembly Instructions

1. Acquire all needed parts
2. Solder headers:
    1. Stacking Headers onto the Feather and two FeatherWings
    2. Male headers on the ADCs, Adafruit sensors, Pololu voltage Regulators, and Arduino Nano (if the one purchased doesn't include one)
    3. Solder female headers into the needed slots on the main PCB.
        1. Feather
        2. Arduino Nano
        3. PMS5003 connection
3. Solder the sensors into their assigned space on the main PCB. (Please see images for locations)
4. Mount the PCB, PMS5003, and AlphaSense sensors to the PCB Base Plate.
5. Attach PCB Base Plate to the `DJI Matrice 600 Upper Expansion Bay Kit`.
