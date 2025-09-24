---
description: How to pick the correct hardware for running StarPilot on a Bolt EV
---

# Vehicle Requirements

> [!WARNING] SuperCruise Bolts Not Supported
> If your Bolt EUV is equipped with SuperCruise, it is not compatible with the Comma or 
> any fork of openpilot at the moment (and likely never will be, sorry).

## Lane Keep Assist System (LKAS)

As with most openpilot compatible cars, the Bolt must be equipped with LKAS (Lane Keep 
Assist System) in order for openpilot to send steering commands. 

### Trim Levels with LKAS
> [!WARNING] Unofficial list
> Just a guide to help new users. Please do your own research.

* 2017-18 EV: Premier trim with Driver Confidence II package [^1] [^2]
* 2019-21 EV: Any trim with Driver Confidence II package [^3] [^4] [^5]
* 2022-23 EV: All trim levels [^6] [^8]
* 2022-23 EUV: All trim levels [^7] [^9]

## Does your Bolt have Adaptive Cruise Control (ACC)?

Both ACC and non-ACC are compatible with StarPilot, 
but vary slightly in hardware recommendations.

### Trim Levels with ACC

* 2022-23 EV: 2LT trim level with Adaptive Cruise Control package [^7] [^9]
* 2022-23 EUV: Premier trim level [^6] [^8]

# Openpilot Hardware List for Bolt

1. [Comma 3X](https://comma.ai/shop/comma-3x)
2. [GM Harness and Harness Box](#gm-harness-and-harness-box)
3. [Comma Pedal](#comma-pedal) (optional, but ***strongly recommended for non-ACC cars***)

> [!TIP] 
> We recommend purchasing from [BearTechWorkshop](https://shop.beartech.ca/) (aka 
> tinybear) whenever possible. They are a small business providing the openpilot community 
> with high quality products and excellent customer support.

> [!NOTE] Comma Power is not needed
> The [Comma Power](https://comma.ai/shop/comma-power) cable is not needed for Bolts. 
> The 12V power is provided by the camera harness 
> and remains on while the car is powered off.

## Comma 3X

Purchase from comma.ai: [Comma 3X](https://comma.ai/shop/comma-3x)

> [!NOTE] Comma 3 End of Life (and Continued Support)
> On 8/26/2025 Comma announced that they are dropping support for the Comma 3 to focus on 
> the Comma 3X. As such, if you are purchasing a new or used Comma, it's probably best to 
> go with a 3X if possible. That being said - there are not currently any technical 
> limitations that prevent the 3 from running the current versions of OpenPilot, as it has 
> the same processor as the 3X. We expect to be able to support the 3 in StarPilot for the 
> foreseeable future.

## GM Harness and Harness Box

The harness and harness box are required for openpilot to communicate with your car.

Purchase from tinybear: [Harness set (Harness Cable + Harness Box)](https://shop.beartech.ca/products/harness-set-gm?variant=44665970688181)

> [!WARNING] Purchasing a harness from Comma
> While you could purchase a harness from Comma, we do not recommend it as it is more 
> expensive and BearTechWorkshop's customer support is better should you run into the rare 
> occurrence of product issues.

> [!CAUTION] Do not purchase a harness box from Comma
> Comma has changed the design of the harness box they sell. It no longer has the RJ45 port 
> and so *cannot* be used with the Comma Pedal.

## Comma Pedal

The Comma Pedal is an interceptor that sits between your throttle pedal and the car.  
When openpilot is disengaged, your throttle pedal is normal.
When openpilot is engaged, openpilot can send its own throttle pedal commands to control
your speed, but will immediately stop sending its own commands when you override or 
disengage.

You always have control, so you can input your own throttle commands at any time, 
overriding openpilot control if it is engaged.
Openpilot will also disengage in the same way as stock CC: when you press the brake pedal, 
throttle pedal, regen paddle, CC cancel button, or CC off button.

Our recommendation for whether or not to purchase the pedal depends on if your car is
[ACC](#acc-bolts) or [Non-ACC](#non-acc-bolts).

### Pedal Purchase List

* [Comma Pedal](https://shop.beartech.ca/products/comma-pedal)
* Ethernet cable
    * At least 10ft long
    * Cat5e is sufficient (higher ratings will be thicker and harder to route under the car's headliner)
    * Flat cables can be easier to route, but quality can be more variable than round cables.
* Optional: [DFU Key](https://shop.beartech.ca/products/dfu-key)
    * tinybear is still making occasional updates to the pedal firmware for Bolts. 
This key is needed to apply those changes. 
See [the pedal firmware page](../pedal-firmware.md) for details.

> [!TIP] Already have a Harness Cable? Bundle your pedal with a harness box.
> If you already have a Harness Cable, but your Harness Box does not have an RJ45 port, 
> you can bundle your Pedal with a 2x9 or 2x13 pin Harness Box - check your specific cable to 
> ensure you purchase the correct box. 

### Non-ACC Bolts

In non-ACC bolts, the Comma Pedal is ***strongly recommended***.
It allows openpilot to accelerate and decelerate using regen braking and one pedal
driving mode (the L gear). It is also capable of stop-and-go (the main reason for comma 
pedal on other vehicles).

The only reasons to not use a pedal interceptor with your non-ACC Bolt are cost or if you 
are uncomfortable with the idea of installing the pedal interceptor.

Without the pedal, openpilot is *very* limited in its ability to control the speed of your 
vehicle. It will operate using a workaround we call "CCLong" or "Redneck ACC". This feature 
emulates a very basic ACC system by using the built-in cruise control system and then 
spamming virtual presses of the + and - buttons to control speed. 

Redneck ACC is able to handle small speed variations while 
following a lead on the highway. However, it is unable to change speed fast enough to 
handle slowing or stopped leads or operate below 24 mph (due to GM limitations), so you 
will be experiencing a small fraction of what openpilot is capable of.


### ACC Bolts

In ACC bolts, openpilot can request gas and brake commands through ACC commands. 
However, due to GM limitations, brake commands only use the friction brakes to slow down 
and regen braking is limited to 10kW (same as coasting in D mode). It also cannot stop-and-go. 

If you'd like 
to use regen & stop-and-go, you can switch your car to CC and install a comma pedal. 
Keep in mind that you lose the ability for openpilot to use the friction brakes if you 
do this. It will be limited to the same deceleration rate as L mode + regen paddle press
(70 kW), the same as non-ACC bolts.

The pedal's capability may extend at a later time with additional hardware or software
changes (resume button harness, virtual pedal tap to just get the car going again with ACC,
etc).


[^1]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2017-bolt.pdf
[^2]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2018-bolt.pdf
[^3]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2019-bolt.pdf
[^4]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2020-boltev.pdf
[^5]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2021-boltev.pdf
[^6]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2022-boltev.pdf
[^7]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2022-bolteuv.pdf
[^8]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2023-boltev.pdf
[^9]: https://cdn.dealereprocess.org/cdn/brochures/chevrolet/2023-bolteuv.pdf
