---
description: How to pick the correct branch and install StarPilot
---

# Install StarPilot

With your car off, plug in your Comma unit. If this is the first time you are booting your Comma, it will first ask for a WiFi connection. If you do not have a stable WiFi connection where your car is, we'd recommend bringing your Comma inside and plugging it in via USB-C to install closer to your WiFi router.

Once your Comma connects to a network, you'll see a screen prompting you to choose software to install. Select **Custom Software**.

This will give you an input box to type in an install link. Find the correct install link for your car below, type it in, and hit continue. StarPilot will then begin installation.

??? "Already have openpilot (or another fork) installed?"

    Reboot your Comma. When you see the comma logo, tap the screen until you see a prompt. This will allow you to reset your Comma and get back to the install screen. Some custom forks have a may have a switcher that will allow you to jump straight to StarPilot. If you are already on StarPilot, there is a switcher to change between branches as needed.

## StarPilot Branches and Install Links

| Car                                        | Gen   | Branch Name    | Install Link                                               |
|--------------------------------------------|-------|----------------|------------------------------------------------------------|
| Chevy Bolt 2022 and later (ACC or non-ACC) | Gen 2 | TorqueTune     | [firestar.link/torque](https://firestar.link/torque)       |
| Chevy Bolt 2018 - 2021                     | Gen 1 | StarPilot      | [firestar.link/starpilot](https://firestar.link/starpilot) |
| Chevy Bolt 2017                            | Gen 0 | StarPilot-2017 | [firestar.link/2017](https://firestar.link/2017)           |
| Non-Volt/Bolt GM w/ACC                     | N/A   | TorqueTune     | [firestar.link/torque](https://firestar.link/torque)       |
| Volt (All Generations) & Other ASCM/SDGM   | N/A   | Kaofui         | [firestar.link/kaofui](https://firestar.link/kaofui)       |
| All Non-GM Cars                            | N/A   | TRX            | [firestar.link/trx](https://firestar.link/trx)             |

> [!WARNING] Stuck on the boot logo after installing?
> See [the faq](../faq.md#im-stuck-on-the-boot-logo-screen-how-do-i-fix-it)

??? note "Why does the 2017 have its own branch?"

    While testing, we discovered that the 2017 has vastly different values for steering torque. This means that, on any other branch of openpilot, 2017 Bolts experience a huge lack of steering ability, when in actuality, they have MORE steering torque than the other gens. This lead us down a long rabbit hole of discovering that lots of things about the 2017 is just... weird and different. Hence the "Gen 0" moniker.
    
!!! info "TRX Branch"

    The TRX branch includes the StarPilot custom model switcher and Visual Only ACC (VOACC) improvements without the Bolt specific things present on other branches. It should be used by any non-GM cars. Check with us in Discord for more specifics

## Dev, Testing, and Other Branches

WIP - More info coming soon.
