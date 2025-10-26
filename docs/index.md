# Introduction
StarPilot is a fork of [FrogPilot](https://github.com/FrogAi/FrogPilot), which itself is a fork of [openpilot](http://github.com/commaai/openpilot). StarPilot runs on the Comma 3 & 3X by [comma_ai](https://comma.ai/).

**openpilot** is an open source driver assistance system. Currently, openpilot performs the functions of Adaptive Cruise Control (ACC), Automated Lane Centering (ALC), Forward Collision Warning (FCW), and Lane Departure Warning (LDW). If you are here, you likely already know what openpilot is.

**FrogPilot** is a fully open-sourced fork of openpilot with a very active and collaborative community. FrogPilot adds features and car support that are not present in stock openpilot.

**StarPilot** started as a fork to improve FrogPilot's operation on various uncooperative models of Chevy Bolt, and has now expanded to provide an improved openpilot experience on supported GM vehicles.

!!! note "Questions?"

    Join us in the [FrogPilot discord](https://discord.com/channels/1137853399715549214/1415794762312581222).

## Credits

These docs were created by Sherloaf Holmes. They are largely based off of the wonderful work of ==ayoba== who created our previous documentation. Shoutout to ==Nik== for always being there to help & answer questions in Discord. And of course, none of this would be possible without ==firestar4430==, who created StarPilot and spends an unadvisable amount of his personal time fixing bugs, creating new features, and answering questions in Discord.

## Community, & Development
StarPilot is developed by firestar4430 and thrives on the testing and feedback of our discord community. If you have questions, bug reports, or want to help test new improvements, join us in the [FrogPilot discord](https://discord.com/channels/1137853399715549214/1415794762312581222)!

## Have the right expectations and ==be safe==

The Comma is best used as a hands-free lane centering and adaptive cruise control device on the highway. It is not capable of safely doing Full Self-Driving (despite Comma’s promotional “Taco Bell run” video) in most scenarios. Using it in complex driving environments is a recipe for a bad time.

In normal chill highway driving, the Comma is quite reliable, but like any driver assistance system, always pay full attention to what’s going on and be ready to take over.

## Changelog

### 10/26/2025
* Add FAQ section

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
