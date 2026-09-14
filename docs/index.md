---
title: StarPilot — Official Wiki & Installation Guide
description: Official StarPilot documentation for comma 3, 3X, and 4. Find installation instructions, supported cars, driving models, Galaxy, and feature guides.
---

# StarPilot: Official Documentation

StarPilot is a community-driven fork of [openpilot](https://github.com/commaai/openpilot).
It runs on the Comma 3, 3X, and 4 by [comma.ai](https://comma.ai/) and is built for people
who want more features, more control over their experience, and room to experiment.

This is the official StarPilot wiki for installation, supported hardware, features, and troubleshooting.

!!! tip "Get $50 off a comma and support StarPilot"

    Buying a comma? **You get $50 off** with [our comma referral link](https://refer.comma.ai/FK49A9V){ rel="sponsored" }.
    **We also receive $50** when you purchase through the link, helping support StarPilot.

StarPilot includes a wide range of driving, tuning, interface, hardware, and developer features.
It supports all three comma devices, Chestnut eGPU, Galaxy remote management, multiple
driving models, and improved support for a growing list of vehicles. See
[Vehicle Compatibility](./cars/support.md) for the full list.

StarPilot began as a fork of [FrogPilot](https://github.com/FrogAi/FrogPilot), and the project
would not exist without FrogPilot and the work behind it. StarPilot has since grown in its own
direction with different hardware support, features, tools, and vehicle improvements.

The project is shaped by the people using it. Feedback, testing, feature ideas, and development
from the community all play a part in where StarPilot goes next.

> [!TIP] Questions? 
> Join us in the [Discord](https://firestar.link/discord)

## New to StarPilot? Start Here.

1. [Get necessary hardware for your car using our car guides](./cars/all.md). 
If you are already running with stock OpenPilot or FrogPilot, 
you can skip this step for now as extra accessories are optional.
1. [Install StarPilot](./software/starpilot.md).
1. Read the [Operation Guide](./usage/operation.md).

## StarPilot features and hardware support

Start with the [StarPilot features overview](./features.md) for capabilities, requirements,
and setup links.

Use these guides to see what each feature does, how to configure it, and its limitations.

| Feature | Official guide |
| --- | --- |
| Supported devices | [StarPilot on comma 3, 3X, and 4](./hardware/comma.md) |
| Remote settings and recordings | [Galaxy web interface](./usage/galaxy.md) |
| Driving model selection | [Driving models](./usage/driving-model.md) and [Chestnut external GPU support](./hardware/chestnut.md) |
| Route guidance | [Navigation with Galaxy](./exclusive/navigation.md) |
| Lane position assistance | [Lane Centering](./exclusive/lane-centering.md) |
| Speed limit sources and offsets | [Speed Limit Controller](./exclusive/speed-limit-controller.md) |
| Parked event recording | [Sentry Mode](./exclusive/sentry-mode.md) |
| Audio and controller pairing | [Bluetooth controls](./exclusive/bluetooth-controls.md) |

Device support and vehicle compatibility are separate. Check the
[vehicle compatibility page](./cars/support.md) and your car's hardware guide before installing.
StarPilot is driver assistance; read the [operation guide](./usage/operation.md) for its limitations.

## How do I install StarPilot?

The stable installer value is `firestar5683/StarPilot`. Enter it on your comma device's
custom software setup screen. Follow the [StarPilot installation guide](./software/starpilot.md)
for comma 3, 3X, and 4 instructions, development builds, and branch switching.

## How is StarPilot related to openpilot and FrogPilot?

StarPilot builds on openpilot and began as a FrogPilot fork. It is a separate community
project with its own development, hardware support, features, and vehicle improvements.
For the implementation, see the [StarPilot source code](https://github.com/firestar5683/StarPilot).
For specific capabilities, use the feature guides above and the [settings guide](./usage/settings.md).

## Official StarPilot links

- [StarPilot wiki](https://wiki.firestar.link/): installation, compatibility, and usage documentation.
- [StarPilot on GitHub](https://github.com/firestar5683/StarPilot): source code and development.
- [StarPilot Discord](https://firestar.link/discord): announcements, community help, and support.
- [FAQ and troubleshooting](./faq.md): common questions and fixes.
- [Support tickets](./ticketsystem.md): report an issue or request an investigation.

## Credits

These docs were created by Sherloaf Holmes. 
They are largely based off of the wonderful work of ==ayoba== who created our previous documentation. 
Shoutout to ==Nik== for always being there to help & answer questions in Discord. 
And of course, none of this would be possible without ==firestar4430==, 
who created StarPilot and spends an unadvisable amount of his personal time fixing bugs, 
creating new features, and answering questions in Discord.

## Community and Development

StarPilot is developed by firestar4430 and thrives on the testing and feedback of our Discord community. 
If you have questions, bug reports, or want to help test new improvements, 
join us in the [Discord](https://firestar.link/discord)!

## Update Notes

Update notes are in the #announcements channel of the [Discord](https://firestar.link/discord).
