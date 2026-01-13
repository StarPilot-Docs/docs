---
description: How to pick the correct hardware for running StarPilot on a Bolt EV
---
# Bolt Hardware

## Vehicle Quirks

Things to be aware of for your vehicle relating to openpilot:

* Openpilot cannot steer below 7 mph.
* Non-ACC Bolts are limited to regen-only braking using a [Comma Pedal](../hardware/comma-pedal.md). 
This means a max 70kW of deceleration meaning no emergency stops 
and poor low-speed slowing performance. 
You will occasionally need to brake manually.
* ACC Bolts are limited to 10kW of regen 
(but unlike non-ACC, openpilot can control your friction brakes).
* ACC Bolts do not have stop and go support (press accelerator pedal or press CC resume).
    * Non-ACC bolts with Comma Pedal do have stop-and-go support.
* *22-23 Bolts only*: Sport mode will decrease available steering torque.
* Steering wheel LKAS button and light do not work when comma is connected (purely a cosmetic issue).
    * If pressed, the dash will display "LKAS is unavailable" but op steering will still work.
    * The button also cannot be used with the openpilot custom button actions 
(ACC models can still use the distance button).

## Vehicle Requirements

> [!WARNING] SuperCruise Bolts Not Supported
> If your Bolt EUV is equipped with SuperCruise, it is not compatible with the Comma or 
> any fork of openpilot at the moment (and likely never will be, sorry).

### Lane Keep Assist System (LKAS)

As with most openpilot compatible cars, the Bolt must be equipped with LKAS (Lane Keep 
Assist System) in order for openpilot to send steering commands. 

#### Trim Levels with LKAS
> [!WARNING] Unofficial list
> Just a guide to help new users. Please do your own research.

* 2017-18 EV: Premier trim with Driver Confidence II package [^1] [^2]
* 2019-21 EV: Any trim with Driver Confidence II package [^3] [^4] [^5]
* 2022-23 EV: All trim levels [^6] [^8]
* 2022-23 EUV: All trim levels [^7] [^9]

### Does your Bolt have Adaptive Cruise Control (ACC)?

Both ACC and non-ACC are compatible with StarPilot, 
but vary slightly in hardware recommendations.

#### Trim Levels with ACC

* 2022-23 EV: 2LT trim level with Adaptive Cruise Control package [^7] [^9]
* 2022-23 EUV: Premier trim level [^6] [^8]

## Openpilot Hardware List for Bolt

1. [Comma 3X](../hardware/comma-3x.md)
2. [GM Harness and Harness Box](../hardware/gm-harness.md)
3. [Comma Pedal](../hardware/comma-pedal.md) (optional, but ***strongly recommended for non-ACC cars***)

{% include-markdown "../hardware/embed/beartech.md" %}
{% include-markdown "../hardware/embed/comma-power.md" %}

### Should I buy a Comma Pedal?

Our recommendation for whether or not to purchase the pedal depends on if your car is
[ACC](#acc-bolts) or [Non-ACC](#non-acc-bolts).

#### Non-ACC Bolts

In non-ACC bolts, the Comma Pedal is ***strongly recommended***.
It allows openpilot to accelerate and decelerate using regen braking and one pedal
driving mode (the L gear). It is also capable of stop-and-go (the main reason for comma 
pedal on other vehicles).

The only reasons to not use a pedal interceptor with your non-ACC Bolt are cost or if you 
are uncomfortable with the idea of installing the pedal interceptor.

Without the pedal, openpilot is *very* limited in its ability to control the speed of your 
vehicle. It will operate 
[using a workaround we call "CCLong" or "Redneck ACC"](../faq.md#what-is-redneck-acc-aka-cc-long). 

#### ACC Bolts

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
