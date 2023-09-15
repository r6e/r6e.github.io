---
layout: default
title: "Elegoo Neptune 4 MCU Guide"
date: "2023-09-11 19:00:00 -0600"
categories: Elegoo "Neptune 4" "3D Printing" Guide
category_title: MCU Guide
---

Many of the guides below involve using `stm32flash`, which should already be installed on your Neptune 4. See the [stm32flash Wiki](https://sourceforge.net/p/stm32flash/wiki/Home/) for details on that tool.

# Entering Bootloader Mode

**WARNING:** In Bootloader mode, it is extremely easy to render your MCU non-bootable, making it impossible to use your printer. It is also difficult to recover from this state. Don't do this unless you're absolutely sure there is no other way.

In order to perform operations on the MCU firmware, it is necessary to first enter the bootloader mode (also referred to as BOOT0). There are two ways to do this.

## Option 1: Software

I could not get this working, but it could be that my firmware has become too messed-up to flash this way. It could also be that they just plain do not work.

### Option 1a: How Elegoo Does It

The Makerbase client, which is the central service for managing the printer, uses the `hid-flash` tool to perform updates. In order to put the MCU into bootloader mode, it toggles the DTR line to low, then back to high.

An easy way to do this manually is to install `picocom` (which is useful for a number of other tasks), and connect to the MCU using the following command:

```bash
picocom /dev/ttyS0
```

Once connected, press `Ctrl+A`, then `Ctrl+P`.

### Option 1b: Using GPIO

It appears as though the `BOOT0` and `BOOT1` lines should be connected to the host using GPIO. If this is the case, I have not yet found the correct GPIO pins. The following use pins 1 and 2 as an example, but those are *definitely* not correct.

Connect to your Neptune 4 either using SSH or a serial console (instructions WIP). Then, run the following code in the terminal:

```bash
stm32flash -i '-2,-1,1:2,-1,,,1' /dev/ttyS0
```

This restarts the MCU into bootloader mode using GPIO, gets information about the connection, then restarts the MCU into normal mode.

## Option 2: Hardware (NOT RECOMMENDED)

**WARNING:** This method involves poking your *powered-on* board with a piece of metal. If you accidentally touch the wrong part, you could fry your board or electrocute yourself.

If the software mode doesn't work, then you can activate the bootloader using a hardware-based method.

1. Shut down your Neptune 4, turn off the power switch, and remove the power plug.
2. Remove the filament spool and any other unattached items.
3. Place the Neptune 4 on its back on a non-abrasive surface. Support the printer with other objects so it is stable and not resting on the stepper motor, print bed, cables, or Y-axis rail.
4. On the underside, toward the front, unscrew the cover over the control board. Be careful not to tug on the fan cable when removing the panel.
5. Reconnect the power plug and either the network or serial connection, depending on whether you intend to connect using SSH or serial.
6. Power on the printer.
7. Connect to your Neptune 4 either using SSH or a serial console (instructions WIP).
8. Locate the pads labeled `BOOT0`. They should be behind the micro SD card slot, on the other side of the `RESET` button.
9. Using a metal implement of appropriate shape and size (such as tweezers), bridge the gap between the two pads. BE VERY CAREFUL TO NOT TOUCH ANY OTHER COMPONENTS!
10. Press the `RESET` button.
11. Wait a few seconds, then in the terminal, run `stm32flash /dev/ttyS0`. If the bootloader is active, it should return some helpful information about the connection.

# Dumping Bootloader Firmware

Simply run:

```bash
# If using the GPIO method
stm32flash -i '-2,-1,1:2,-1,,,1' -r firmware-backup.bin /dev/ttyS0

# If not
stm32flash -r firmware-backup.bin /dev/ttyS0
```
