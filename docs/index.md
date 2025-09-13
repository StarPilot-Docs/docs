# Introduction
StarPilot is a fork of [FrogPilot](https://github.com/FrogAi/FrogPilot), which itself is a fork of [openpilot](http://github.com/commaai/openpilot). StarPilot runs on the Comma 3 & 3X by [comma_ai](https://comma.ai/).

**openpilot** is an open source driver assistance system. Currently, openpilot performs the functions of Adaptive Cruise Control (ACC), Automated Lane Centering (ALC), Forward Collision Warning (FCW), and Lane Departure Warning (LDW). If you are here, you likely already know what openpilot is.

**FrogPilot** is a fully open-sourced fork of openpilot with a very active and collaborative community. FrogPilot adds features and car support that are not present in stock openpilot.

**StarPilot** started as a fork to improve FrogPilot's operation on various uncooperative models of Chevy Bolt, and has now expanded to provide an improved openpilot experience on supported GM vehicles.

!!! note "Questions?"

    Join us in the [#starpilot-troubleshooting](https://discord.com/channels/1137853399715549214/1415794830965080155) or [#starpilot-discussion](https://discord.com/channels/1137853399715549214/1415794762312581222) channels of the [FrogPilot discord](https://discord.gg/frogpilot).

## Credits

These docs were created by Sherloaf Holmes. They are largely based off of the wonderful work of ==ayoba== who created our previous documentation. Shoutout to ==Nik== for always being there to help & answer questions in Discord. And of course, none of this would be possible without ==firestar4430==, who created StarPilot and spends an unadvisable amount of his personal time fixing bugs, creating new features, and answering questions in Discord.

## Community, & Development
StarPilot is developed by firestar4430 and thrives on the testing and feedback of our discord community. If you have questions, bug reports, or want to help test new improvements, join us in the [#starpilot-troubleshooting](https://discord.com/channels/1137853399715549214/1415794830965080155) or [#starpilot-discussion](https://discord.com/channels/1137853399715549214/1415794762312581222) channels of the [FrogPilot discord](https://discord.gg/frogpilot)!

## Have the right expectations and ==be safe==

The Comma is best used as a hands-free lane centering and adaptive cruise control device on the highway. It is not capable of safely doing Full Self-Driving (despite Comma’s promotional “Taco Bell run” video) in most scenarios. Using it in complex driving environments is a recipe for a bad time.

In normal chill highway driving, the Comma is quite reliable, but like any driver assistance system, always pay full attention to what’s going on and be ready to take over.

## Changelog

### 9/13/2025
* Updated discord links for new StarPilot discord channels

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
