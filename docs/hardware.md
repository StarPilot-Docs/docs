---
description: How to pick the correct hardware for running StarPilot on a Bolt 
---

# Required Hardware
Our current hardware recommendations are as follows:

## Chevy Bolt with ACC
You have ACC if your car is an EV or EUV from 2022-2023 and came equipped with the 2LT Trim with Adaptive Cruise Control Package.

Your car is supported by upstream openpilot. It will use the friction breaks to slow down, but will not use regen breaking, or have stop-and-go. If you'd like to use regen & stop-and-go, you can switch your car to CC and use a pedal, in which case you'd want to follow the non-ACC section. Keep in mind that you lose the ability for openpilot to use the friction breaks if you do this. 

This capability may extend at a later time with additional hardware (resume button harness, pedal to just get the car going again, etc).

??? warning "SuperCruise Bolts Not Supported"

    If your Bolt EUV is equiped with SuperCruise, it is not compatible with the Comma or any fork of openpilot at the moment (and likely never will be, sorry).

### From comma_ai

* [Comma 3X (or 3) with GM Harness & Harness Box](https://comma.ai/shop/comma-3x?harness=Chevrolet%2520Bolt%2520EV%25202022-23)



???+ note
    
    If you have any interest in trying the comma pedal now or in the future, you should not purchase the harness & harness box with your Comma, and instead get the [Harness set from tinybear](https://shop.beartech.ca/products/harness-set-gm?variant=44665970688181). The newer harness boxes from Comma no longer include the RJ45 port necessary for pedal use.
    
## Chevy Bolt without ACC
This includes all 2017-2021 Bolts, as well as 2022-2023 Bolts without the Adaptive Cruise Control Package. 

### From comma_ai:

* [Comma 3X (or 3)](https://comma.ai/shop/comma-3x)

??? warning "Do not purchase a harness from Comma"

    Comma has changed the design of the harness box & harness they ship with the 3X, and they no longer have the RJ45 port required for pedal use. See the next section for more info.
    
### From [BearTechWorkshop](https://shop.beartech.ca/) (aka tinybear):

* [Comma Pedal](https://shop.beartech.ca/products/comma-pedal)
* [Harness set (Harness Cable + Harness Box)](https://shop.beartech.ca/products/harness-set-gm?variant=44665970688181)
* Optional: [DFU Key](https://shop.beartech.ca/products/dfu-key)
    * tinybear is still making occasional updates to the pedal firmware for Bolts. This key is needed to apply those changes. Free shipping if purchased with your Pedal.

??? note "Already have a Harness Cable?"

    If you already have a Harness Cable, but your Harness Box does not have an RJ45 port, you can get your Pedal with a 2x9 or 2x13 pin Harness Box - check your specific cable to ensure you purchase the correct box.
    
### From your cable supplier of choice:

* Flat Cat5e cable, at least 10ft long

??? note "A note on "Redneck ACC""

    Without the pedal, openpilot is unable to control the throttle of your car. If you are uncomfortable with the idea of installing the pedal intercepter, it is possible to operate using a workaround we call "CCLong" or "Redneck ACC", using just the Comma unit, harness, and harness box. This feature emulates a very basic ACC system by activating your cars basic cruise control and then spamming virtual presses of the + and - buttons to control speed. The system is able to handle very simple speed variations while following a lead on the highway. However, it is unable to change speed fast enough to handle slowing or stopped leads or operate below 24 mph (due to GM limitations), so you will be experiencing a small fraction of what openpilot is capable of. 