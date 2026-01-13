---
description: How to pick the correct branch and install StarPilot
---

# Install StarPilot

With your car off, plug in your Comma unit. If this is the first time you are booting your Comma, it will ask for a WiFi connection. If you do not have a stable WiFi connection where your car is, we'd recommend bringing your Comma inside and plugging it in via USB-C to install closer to your WiFi router.

Once your Comma connects to a network, you'll see a screen prompting you to choose software to install. Select **Custom Software**.

## Recommended Installer

Use `install.firestar.link` for all vehicles. This dynamic installer asks a few questions
about your car and automatically selects the correct branch.
This reduces guesswork when choosing a branch.

If the installer fails or a manual install is required, follow the directions below.

<video controls width="100%">
  <source src="/assets/videos/install.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

If you are installing manually, find the correct install link for your car below, type it in, and hit continue. StarPilot will then begin installation.

??? "Already have openpilot (or another fork) installed?"

    Reboot your Comma. When you see the comma logo, tap the screen until you see a prompt. This will allow you to reset your Comma and get back to the install screen. Some custom forks include a switcher that allows you to jump straight to StarPilot. If you are already on StarPilot, there is a switcher to change between branches as needed.

## StarPilot Branches and Install Links

Use `install.firestar.link` by default; use manual links only when required.

| Car                                        | Gen   | Branch Name    | Install Link                                               |
|--------------------------------------------|-------|----------------|------------------------------------------------------------|
| Chevy Bolt 2022 and later (ACC or non-ACC) | Gen 2 | TorqueTune     | [firestar.link/torque](https://firestar.link/torque)       |
| Chevy Bolt 2018 - 2021                     | Gen 1 | StarPilot      | [firestar.link/starpilot](https://firestar.link/starpilot) |
| Chevy Bolt 2017                            | Gen 0 | StarPilot-2017 | [firestar.link/2017](https://firestar.link/2017)           |
| GM Vehicles with ACC (except Volt)         | N/A   | TorqueTune     | [firestar.link/torque](https://firestar.link/torque)       |
| Volt                                       | N/A   | Kaofui         | [firestar.link/kaofui](https://firestar.link/kaofui)       |
| All Non-GM Cars                            | N/A   | TRX            | [firestar.link/trx](https://firestar.link/trx)             |

> [!WARNING] Stuck on the boot logo after installing?
> See [the faq](../faq.md#im-stuck-on-the-boot-logo-screen-how-do-i-fix-it)

> [!WARNING] Install failing and taking you back to the same install screen?
> Use installer.comma.ai/firestar5683/BranchNameHere

> [!WARNING] Other install issues
> Message us in [Discord](https://firestar.link/discord) 
> or [flash your comma](https://flash.comma.ai) and retry.

> [!NOTE] Why does the 2017 have its own branch?
> While testing, we discovered that the 2017 has vastly different values for steering torque. 
> This means that, on any other branch of openpilot, 2017 Bolts experience a huge lack of 
> steering ability, when in actuality, they have MORE steering torque than the other gens. 
> This lead us down a long rabbit hole of discovering that lots of things about the 2017 is just... 
> weird and different. Hence the "Gen 0" moniker.
    
> [!NOTE] TRX Branch
> The TRX branch includes the StarPilot custom model switcher and Visual Only ACC (VOACC) 
> improvements without the Bolt specific things present on other branches. 
> It should be used by any non-GM cars. 
> Check with us in [Discord](https://firestar.link/discord) for more specifics.

## Dev, Testing, and Other Branches

WIP - More info coming soon.
