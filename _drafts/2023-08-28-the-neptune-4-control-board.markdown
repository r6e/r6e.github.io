---
layout: default
title: "The Neptune 4 Control Board"
date: "2023-08-28 08:00:00 -0600"
categories: Elegoo "Neptune 4" "3D Printing" Hardware
---

{% picture ZNP_K1_V1-0.jpg --alt Neptune 4 Control Board %}

The Neptune 4 uses a ZNP K1 v1.0 control board. There is not much information on this exact board, aside from a brief overview in the article [Elegoo Neptune 4 3D Printer in Review](https://www.igorslab.de/en/elegoo-neptune-4-3d-drucker-im-test/5/). According to the Reddit post [Am I crazy or is the Neptune 4 (Pro) just not a great deal?](https://www.reddit.com/r/ElegooNeptune3/comments/13zni3g/am_i_crazy_or_is_the_neptune_4_pro_just_not_a/), it is a clone of the [MKS Skipr](https://github.com/makerbase-mks/MKS-SKIPR). However, there are some significant differences between the two.


# Specifications

| **SOC** | [RK3328](https://www.rock-chips.com/a/en/products/RK33_Series/2017/0118/829.html) |
| **RAM** | 8GB DDR3 933 [M15T4G16256A–DEBG2[S/C]](https://www.esmt.com.tw/en/Products/DRAM/DDR3(L)%20SDRAM-1-4) |
| **Storage** | [KLM8G1GETF-B041](https://semiconductor.samsung.com/estorage/emmc/emmc-5-1/klm8g1getf-b041/) eMMC |
| **Microcontroller** | [STM32F402RCT6](https://www.st.com/en/microcontrollers-microprocessors/stm32f401rc.html) |
| **Drivers** | [TMC2209](https://www.trinamic.com/products/integrated-circuits/details/tmc2209-la/) |
| **Serial Adapter** | [CH340C](https://wch-ic.com/products/CH340.html) |

# Interfaces

{% picture ZNP_K1_V1-0_interfaces.jpg --alt Control board interface locations %}

## Ports
* 10/100/1000 Ethernet
* UART (RJ-11)
* UART (4-pin, unpopulated)
* USB-A 3.0
* USB-C (Serial communication only)
* Micro SD
* USB-A 2.0 (Unpopulated)

## Pins/Headers/Connectors

* ADXL345
* EMMC

### Lights/Fans

* LED1 (Model light)
* LED2 (Lighting)
* FAN1 (Print head fan)
* FAN2 (Model fan)
* FAN3 (Controller board fan)

### Sensors

* S G 24v / Level (Proximity switch)
* PWOFF (unused)
* DET0 (Filament detector 0)
* DET1 (Filament detector 1)
* Z+/Z-/Y-/X- (Endstops)
* TB0 (Heatbed thermistor)
* TB1 (Heatbed thermistor)
* TH1 (Hotend thermistor)

### Steppers

* X (X-axis stepper)
* Y (Y-axis stepper)
* Z (Z-axis stepper)
* E0 (Extruder 0 stepper)
* E1 (Extruder 1 stepper)
* EN STEP DIR G (External driver stepper board)

# Jumpers/Buttons

* M0/M1/M2 (Microstep mode select jumper for E1)
* UART (UART mode jumper for E1)
* XDIAG/YDIAG/ZDIAG/E0DIAG/E1DIAG (Sensorless homing jumper)
* Unknown 6-pin (possibly unused jumpers to toggle IC functionality)
* RST (MCU Reset button)
* H-RST (Host reset button)
* BOOT0 (Enable DFU mode, button missing)

## Power

* 12/24V (Supply)
* HB0 (Heatbed)
* HB1 (Heatbed)
* HE0 (Hotend)
