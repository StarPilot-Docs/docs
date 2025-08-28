---
description: How to pick the correct hardware for running StarPilot on a Volt
---

# Required Hardware - Volt & Other ASCM/SDGM Cars
The Volt has a number of possible configurations. This page lists the recommended method per car type, and all possible methods.

There are two parts to OpenPilot control: Lateral Control (Steering) & Longitudinal Control (Gas/Brake).

ASCM & SDGM give the comma control over steering, and it will use your cars built in ACC. SASCM allows you to override the built in ACC and use OpenPilot Longitudinal control. If you have stock ACC and do not wish to use OpenPilot Long, you can just purchase the ASCM/SDGM portion of the suggestions.

## Recommended Config per Car Model
* 2017-2018 Chevy Volt with Factory ACC: [ASCM Harness & SASCM](#ascm-harness-sascm)
* 2019 Chevy Volt with Factory ACC: [SDGM Harness & SASCM](#sdgm-harness-sascm)
* Flashed Volts (With no windshield camera): [OBD-II Harness](#obd-ii-harness)
* Non-Volt Car with ASCM: [ASCM Harness & SASCM](#ascm-harness-sascm)
* Non-Volt Car with SDGM: [SDGM Harness & SASCM](#sdgm-harness-sascm)

??? info "Comma 3 End of Life (and Continued Support)"

    On 8/26/2025 Comma announced that they are dropping support for the Comma 3 to focus on the Comma 3X. As such, if you are purchasing a new or used Comma, it's probably best to go with a 3X if possible. That being said - there are not currently any technical limitations that prevent the 3 from running the current versions of OpenPilot, as it has the same processor as the 3X. We expect to be able to support the 3 in StarPilot for the forseeable future.

## ASCM Harness & SASCM

### From comma_ai:

* [Comma 3X](https://comma.ai/shop/comma-3x)

??? warning "Do not purchase a harness from Comma"

    Comma has changed the design of the harness box & harness they ship with the 3X, and they no longer have the RJ45 port required for pedal use. See the next section for more info.

### From [BearTechWorkshop](https://shop.beartech.ca/) (aka tinybear):

* [ASCM Harness Plus + Harness Box](https://shop.beartech.ca/products/ascm-harness?variant=44900990124213)
* [SASCM](https://shop.beartech.ca/products/sascm-for-gm-vehicles)
* Optional: [Comma Pedal](https://shop.beartech.ca/products/comma-pedal) for ability to start from a stop on 2018 or newer.

??? note "Already have a Harness Cable?"

    If you already have a Harness Cable, but your Harness Box does not have an RJ45 port, you can get your Pedal with a 2x9 or 2x13 pin Harness Box - check your specific cable to ensure you purchase the correct box.

### From your cable supplier of choice:

* Optional: If buying a Comma Pedal Only: Flat Cat5e cable, at least 10ft long



## SDGM Harness & SASCM

### From comma_ai:

* [Comma 3X](https://comma.ai/shop/comma-3x)

??? warning "Do not purchase a harness from Comma"

    Comma has changed the design of the harness box & harness they ship with the 3X, and they no longer have the RJ45 port required for pedal use. See the next section for more info.

### From [BearTechWorkshop](https://shop.beartech.ca/) (aka tinybear):

* [SDGM Harness + Harness Box](https://shop.beartech.ca/products/sdgm-harness)
* [SASCM](https://shop.beartech.ca/products/sascm-for-gm-vehicles)
* Optional: [Comma Pedal](https://shop.beartech.ca/products/comma-pedal) for ability to start from a stop.

??? note "Already have a Harness Cable?"

    If you already have a Harness Cable, but your Harness Box does not have an RJ45 port, you can get your Pedal with a 2x9 or 2x13 pin Harness Box - check your specific cable to ensure you purchase the correct box.

### From your cable supplier of choice:

* Optional: If buying a Comma Pedal Only: Flat Cat5e cable, at least 10ft long


## OBD-II Harness

### From comma_ai:

* [Comma 3X](https://comma.ai/shop/comma-3x)
* One of the following two OBD Harnesses:
  * [OBD-II Harness](https://comma.ai/shop/car-harness?harness=OBD-II) - Can be purchased with your Comma if buying a new one.
  * [Konik OBD2C connector](https://konik.ai/shop/obd2c-connector/) - Cheaper option. Confirmed by a community member to work as an OBD harness for Volts that need it. Note that this does not come with a USB-C cable, so you will need to supply your own cabling.
