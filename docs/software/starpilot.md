---
description: How to install StarPilot
---

# Install StarPilot

With your car off, plug in your Comma unit. If this is the first time you are booting your Comma, it will ask for a WiFi connection. If you do not have a stable WiFi connection where your car is, we'd recommend bringing your Comma inside and plugging it in via USB-C to install closer to your WiFi router.

Once your Comma connects to a network, you'll see a screen prompting you to choose software to install. Select **Custom Software**.

## Recommended Installer

Use `install.firestar.link` for all vehicles.

The installer now has three options:

1. `Install` (recommended for almost everyone)
2. `Choose a special branch` (advanced users/testing only)
3. `Deep Nuke Params` (if you're coming from FrogPilot or an older setup and get stuck on the boot logo, use this to wipe old stuck parameters)

If you are currently on an older or special branch, you can use `install.firestar.link` and pick `Install` to move to the main StarPilot branch.

> [!NOTE] Bolt fingerprint year matters
> Make sure your Bolt fingerprint has the correct model year selected.
> Each Bolt year has its own lateral tuning.
> Only the 2017 Bolt fingerprint supports the higher 4.5Nm torque limits.
> Do not select the 2017 fingerprint on other model years. It will not give more steering torque,
> but will prevent you from getting proper steering safety alerts.
> Auto fingerprint usually gets this right, but if steering behavior looks wrong, verify your
> fingerprint in [Vehicle Controls](../usage/settings.md#vehicle-controls).

<video controls width="100%">
  <source src="/assets/videos/install.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

??? "Already have openpilot (or another fork) installed?"

    Reboot your Comma. When you see the comma logo, tap the screen until you see a prompt. This will allow you to reset your Comma and get back to the install screen. Some custom forks include a switcher that allows you to jump straight to StarPilot.

> [!WARNING] Stuck on the boot logo after installing?
> See [the faq](../faq.md#im-stuck-on-the-boot-logo-screen-how-do-i-fix-it)

> [!WARNING] Install failing and taking you back to the same install screen?
> Retry `install.firestar.link`. If it still loops, [flash your comma](https://flash.comma.ai) and retry.

> [!WARNING] Other install issues
> Message us in [Discord](https://firestar.link/discord)
> or [flash your comma](https://flash.comma.ai) and retry.

## Dev, Testing, and Other Branches

WIP - More info coming soon.
