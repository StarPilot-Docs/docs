---
description: How to pick the correct hardware for running StarPilot on a Volt 
---

# Required Hardware
The Volt has a number of possible configurations. This page lists the recommended method per car type, and all possible methods. 

There are two parts to OpenPilot control: Lateral Control (Steering) & Longitudinal Control (Gas/Brake).

ASCM & SDGM give the comma control over steering, and it will use your cars built in ACC. SASCM allows you to override the built in ACC and use OpenPilot Longitudinal control. If you have stock ACC and do not wish to use OpenPilot Long, you can just purchase the ASCM/SDGM portion of the suggestions. 

## Recommended Config per Car Model
* 2016-2018 Chevy Volt with Factory ACC: [ASCM Harness & SASCM](#ascm-harness-sascm)
* 2019 Chevy Volt with Factory ACC: [SDGM Harness & SASCM](#sdgm-harness-sascm)
* Flashed Volts (With no windshield camera): [OBD + L&P Harnesses](#obd-lp-harnesses)
* Non-Volt Car with ASCM: [ASCM Harness & SASCM](#ascm-harness-sascm)
* Non-Volt Car with SDGM: [SDGM Harness & SASCM](#sdgm-harness-sascm)


## ASCM Harness & SASCM

### From comma_ai:

* [Comma 3X (or 3)](https://comma.ai/shop/comma-3x)

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

* [Comma 3X (or 3)](https://comma.ai/shop/comma-3x)

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


## OBD + L&P Harnesses

### From comma_ai:

* [Comma 3X (or 3)](https://comma.ai/shop/comma-3x)

??? warning "Do not purchase a harness from Comma"

    Comma has changed the design of the harness box & harness they ship with the 3X, and they no longer have the RJ45 port required for pedal use. See the next section for more info.
    
### From [BearTechWorkshop](https://shop.beartech.ca/) (aka tinybear) & [L&P](https://leepauldinginc.square.site):

* [OBD Power](https://shop.beartech.ca/products/obd-and-splitter?variant=45069621625013)
* [L&P Harness](https://leepauldinginc.square.site/product/gm-volt-malibu-harness-for-open-pilot/20)
