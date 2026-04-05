---
description: How to install StarPilot
---

# Install StarPilot

With your car off, plug in your Comma unit. 
You may instead plug it in using a USB-C adapter while in your home 
(this may be a better option if Wi-Fi signal is poor in your car).

Immediately after plugging it in, tap on the screen repeatedly until you see a reset screen.
If you miss the reset screen, unplug it, wait 60 seconds, then try again.

# Comma 4

1. Swipe to reset.
2. Connect to Wi-Fi.
3. Install custom software.
4. Enter the link `firestar5683/StarPilot`

# Comma 3/3x

1. Tap reset.
2. Connect to Wi-Fi.
3. Install custom software.
4. When prompted for an install link:
   1. If coming from openpilot or sunnypilot, use `firestar5683/StarPilot`.
   2. If coming from a different fork, use `install.firestar.link`. 
Choose the default `Install` option.
See [Custom StarPilot Installer](#custom-starpilot-installer) for more details if you have trouble.

> [!WARNING] Stuck on the boot logo after installing?
> See [the faq](../faq.md#im-stuck-on-the-boot-logo-screen-how-do-i-fix-it)

> [!WARNING] Other install issues
> Message us in [Discord](https://firestar.link/discord)
> or [flash your comma](https://flash.comma.ai) and retry.

> [!TIP] Want to change settings from your phone?
> Use [the Galaxy](../usage/galaxy.md)

> [!NOTE] Bolt fingerprint year matters
> Make sure your Bolt fingerprint has the correct model year selected.
> Each Bolt year has its own lateral tuning.
> Only the 2017 Bolt fingerprint supports the higher 4.5Nm torque limits.
> Do not select the 2017 fingerprint on other model years. It will not give more steering torque,
> but will prevent you from getting proper steering safety alerts.
> Auto fingerprint usually gets this right, but if steering behavior looks wrong, verify your
> fingerprint in [Vehicle Controls](../usage/settings.md#vehicle-controls).

## Custom StarPilot Installer

`install.firestar.link` is StarPilot's custom installer. 

> [!WARNING] This installer currently has some limitations
> Only works for Comma 3/3x and on older AGNOS forks. 
> Do not use if coming from openpilot or sunnypilot.

The installer now has three options:

1. `Install` (recommended for almost everyone)
2. `Choose a special branch` (advanced users/testing only)
3. `Deep Nuke Params` (if you're coming from FrogPilot or an older setup and get stuck on the boot logo, use this to wipe old stuck parameters)

If you are currently on an older or special branch, you can use `install.firestar.link` and pick `Install` to move to the main StarPilot branch.

<video controls width="100%">
  <source src="/assets/videos/install.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
