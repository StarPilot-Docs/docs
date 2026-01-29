# Pedal Firmware Flashing

!!! warning "Gen1 Bolts ONLY (2017-2021)"

!!! warning

    If you purchased your pedal before June 2025 and have not updated the firmware, you will encounter issues with the current version of StarPilot.

The Gen1 Bolt firmware released in October 2024 ran at twice the speed it should have. This was corrected in June 2025. Firmware prior to October 2024 will run okay, but the newer firmware is better, so it is best to update.

## Required Resources

* [DFU Key](https://shop.beartech.ca/products/dfu-key)
* [bootstub.pedal.bin](../assets/pedal-firmware/gen1-bolt/bootstub.pedal.bin){:download="bootstub.pedal.bin"}
* [pedal.bin](../assets/pedal-firmware/gen1-bolt/pedal.bin){:download="pedal.bin"}

!!! note "USB cable requirement"

    USB-C to USB-C does not work for DFU flashing. There must be a USB-A port somewhere in the chain (for example, USB-A to USB-C or USB-A to micro-USB).
    The DFU key/pedal is a USB 2.0 device and does not include USB-C circuitry, so a C-to-C cable often will not provide VBUS or enumerate the device.


## Flashing Instructions

[Flash Comma Pedal in DFU Mode Tutorial from TinyBear](https://www.youtube.com/watch?v=DNf0OGwXUUQ)

## Other Firmwares

The full list of available pedal firmwares for other cars is available at tinybear's GitHub repo [here.](https://github.com/fraserxiong/panda_firmware/tree/master)
