# Introduction

StarPilot is a fork of [FrogPilot](https://github.com/FrogAi/FrogPilot), 
which itself is a fork of [openpilot](http://github.com/commaai/openpilot). 
StarPilot runs on the Comma 3 and 3X by [comma.ai](https://comma.ai/).

> [!WARNING] Comma 4 Support
> Comma has released the Comma 4, but StarPilot depends on FrogPilot's base for new device support.
> Once FrogPilot rebases and adds Comma 4 support, we will begin the StarPilot migration.
> In the meantime, we maintain a SunnyPilot testing branch (`firestar.link/sunnypedal`) with full GM lateral and pedal support.
> It does not include StarPilot's advanced features (e.g., paddle integration and VoACC tuning),
> but it can get you running on a pedal interceptor or a non‑adaptive‑cruise GM vehicle.
> This branch is functional and intended to get pedal interceptor and non‑ACC GM vehicles up and running.
> It is not a primary focus and is not actively monitored, so if anything seems off, please reach out in [Discord](https://firestar.link/discord).

**openpilot** is an open-source driver assistance system. 
Currently, openpilot performs the functions of Adaptive Cruise Control (ACC), 
Automated Lane Centering (ALC), and Lane Departure Warning (LDW). 
If you are here, you likely already know openpilot.

**FrogPilot** is a fully open-sourced fork of openpilot with a very active 
and collaborative community. FrogPilot adds features and car support 
that are not present in stock openpilot.

**StarPilot** is a fork of FrogPilot that provides better tuning for radar-less/VoACC cars
and GM cars.

> [!TIP] Questions? 
> Join us in the [FrogPilot Discord](https://firestar.link/discord)

## New to StarPilot? Start Here.

1. [Get necessary hardware for your car using our car guides](./cars/all.md). 
If you are already running with stock openpilot or FrogPilot, 
you can skip this step for now as extra accessories are optional.
1. [Install StarPilot](./software/starpilot.md).
1. Read the [Operation Guide](./usage/operation.md).

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

## Changelog

### 1/12/2026
* Add Comma 4 notice with SunnyPilot interim branch info
* General Rewrites & Cleanup

### 1/12/2026
* Update settings guidance, including Golden Safety Rule, advanced lateral tuning defaults, and custom torque controller notes
* Refresh driving model recommendations and point users to StarPilot favorites for current picks
* Clarify FAQ guidance for Cruise Fault (ACC-only) and Controls Mismatch fallback steps
* Add install.firestar.link guidance and installer demo video to the Install StarPilot page

### 11/8/2025
* Add more volt non-ACC information
* Add start here to homepage

### 10/26/2025
* Add FAQ section
* Add docker compose file for local dev
* Update non-ACC volt section for with and without flashing.

### 10/16/2025
* Update hardware requirements for LKAS
* Re-organize hardware requirements to reduce duplicated sections

### 10/12/2025
* Updated recommended models: Green Watermelon v8 as primary favorite, Steam Powered v2 as secondary, Firehose as default in frogpilot; removed WD-40, Vikander, and TR suggestions
* Changed Curve Detected Ahead to leave off in lieu of new Curve Speed Controller
* Updated Curve Speed Control description to explain learning user preferences and training icon
* Replaced "Hate a model?" note with warning to always turn off Human Like Accel/Leads
* Fixed spelling of "Accell" to "Accel"
* Removed outdated Vik/Vicky branch note from install page

### 10/2/2025
* Fix broken Discord links
* Update model suggestion to Firehose
* Fix references to old Discord thread setup

### 9/13/2025
* Added TRX branch (for non-GM cars) to the Install StarPilot page
* Updated Discord links to new StarPilot channel

### 9/10/2025
* Updated Human Like recommendations to ==OFF== due to new tuning improvements
* Added Green Watermelon v5 & Firehose to the recommended models

### 8/27/2025
* Added a changelog
* Added info about Comma discontinuing support for the Comma 3
* Updated model recommendations
    * Now suggesting Steam Powered v2 as starter model
* Added Konik OBD2C harness to Volt docs
* Clarified Gen1 Bolt pedal firmware update notices
* Cleaned up formatting
