# Introduction

StarPilot is a fork of [FrogPilot](https://github.com/FrogAi/FrogPilot), 
which itself is a fork of [openpilot](http://github.com/commaai/openpilot). 
StarPilot runs on the Comma 3 & 3X by [comma_ai](https://comma.ai/).

**openpilot** is an open source driver assistance system. 
Currently, openpilot performs the functions of Adaptive Cruise Control (ACC), 
Automated Lane Centering (ALC), and Lane Departure Warning (LDW). 
If you are here, you likely already know what openpilot is.

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

## Community, & Development

StarPilot is developed by firestar4430 and thrives on the testing and feedback of our discord community. 
If you have questions, bug reports, or want to help test new improvements, 
join us in the [Discord](https://firestar.link/discord)!

## Changelog

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
