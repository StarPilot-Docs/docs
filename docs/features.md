---
title: Features, Galaxy & Hardware Support
description: Explore StarPilot features for comma 3, 3X, and 4, including Galaxy, driving models, navigation, speed control, Sentry Mode, and Bluetooth.
---

# StarPilot Features

StarPilot combines openpilot driver assistance with driving model selection, vehicle tuning,
and Galaxy device management. It supports **comma 3, comma 3X, and comma 4** and began as
a FrogPilot fork. This overview links to the setup instructions and limitations for each feature.

For installation, use the [official StarPilot install guide](./software/starpilot.md).

## Features at a glance

| Feature | What you can do | Requirements and limits |
| --- | --- | --- |
| [Galaxy](./usage/galaxy.md) | Manage settings, models, software, logs, and recordings from a browser. | Pair your device; remote access requires connectivity. |
| [Driving models](./usage/driving-model.md) | Choose a model through the model manager. | Model availability depends on hardware; some need Chestnut. |
| [Navigation](./exclusive/navigation.md) | Set destinations in Galaxy and give the model route guidance. | Requires a Mapbox key and navigation toggles. The driver remains responsible for turns and exits. |
| [Lane Centering](./exclusive/lane-centering.md) | Bias the model's path toward the center of detected lane lines. | Experimental; falls back to the normal model path when conditions are unsuitable. |
| [Speed Limit Controller](./exclusive/speed-limit-controller.md) | Configure speed-limit sources, offsets, confirmation, and fallback behavior. | Source availability varies, and reported limits can be wrong. |
| [Sentry Mode](./exclusive/sentry-mode.md) | Review images captured after sustained movement while parked. | Experimental; uses the device accelerometer and requires the device to remain powered. |
| [Bluetooth controls](./exclusive/bluetooth-controls.md) | Pair audio devices and map controller buttons to favorites. | Experimental; check the guide for tested accessories and pairing steps. |

## Galaxy: manage StarPilot from your phone

Galaxy is StarPilot's web interface. Pair it with your comma device to search settings,
select models, change software branches, view recordings, and inspect troubleshooting logs.
You can access it locally or remotely, and bookmark each device's pairing URL if you have
more than one comma.

Its tuning tools include live plots, lateral tuning, and a view of settings that differ from
defaults. These help you describe a problem when [opening a support ticket](./ticketsystem.md).

[Set up Galaxy](./usage/galaxy.md).

## Driving models and optional Chestnut support

The model manager lets you select driving models instead of staying with one fixed choice.
Model preferences vary with the car, roads, and driving conditions; the current model-manager
list is the place to check StarPilot favorites.

Most models use the comma device's built-in processing. StarPilot also supports
[Chestnut external GPU hardware](./hardware/chestnut.md) on comma 3, 3X, and 4. Models that
require an external GPU are labeled, and StarPilot enables them only when the hardware is ready.
Chestnut is optional for standard on-device models.

[Read the driving model guide](./usage/driving-model.md).

## Navigation through Galaxy

Search for a destination, compare routes, and save favorites in Galaxy. StarPilot sends route
information to the comma device, displays turn instructions, and provides upcoming maneuver
information to the driving model. Route Speed Control can help slow for upcoming maneuvers.

Setup requires a Mapbox key, **Use Route Desires**, and **Use Route Speed Control**.
Navigation is a driving aid: it does not guarantee the car will complete a route or make an exit.

[Configure navigation](./usage/settings.md#navigation) and [learn how route guidance works](./exclusive/navigation.md).

## Steering, speed, and driving preferences

StarPilot offers settings for lateral tuning, driving personalities, curve speed control,
and switching between Chill and Experimental modes. Availability and behavior depend on
your vehicle's steering and longitudinal capabilities.

The experimental **Lane Centering** feature adjusts the model's path using detected lane
lines when conditions allow. Its settings include lane offset and the model's authority
to deviate from the lane center. This particular feature is separate from the general
lane-centering assistance provided by openpilot.

**Speed Limit Controller** can use map data, supported dashboard limits, and optional
camera-based sign detection. You can require confirmation before applying a new limit,
set offsets, and choose what happens when source data is missing.

Start with the [settings guide](./usage/settings.md), then read the
[operation guide](./usage/operation.md) for the behavior and limitations of driving controls.

## Sentry Mode and Bluetooth accessories

**Sentry Mode** detects sustained movement through the comma device's accelerometer while
parked and captures camera images. Galaxy provides event history, sensitivity settings,
and notification options. It is motion-triggered event capture; it does not continuously
watch camera video for every person passing the car.

**Bluetooth** support is available on comma 3, 3X, and 4 for audio and controller input.
Galaxy provides pairing and button mapping. The comma 3 and 3X also have Bluetooth
management in the on-device Big UI. Both Sentry Mode and Bluetooth are documented as experimental.

[Set up Sentry Mode](./exclusive/sentry-mode.md) or [pair Bluetooth accessories](./exclusive/bluetooth-controls.md).

## Supported devices and cars

StarPilot supports comma 3, 3X, and 4, but device support does not establish compatibility
with a particular car. The vehicle's year, trim, steering system, ACC configuration, and
installed harness or pedal determine which controls are available.

StarPilot's vehicle work extends beyond GM. The compatibility guide lists additions and
improvements across multiple manufacturers, while the car guides explain specific hardware setups.

- [Compare comma devices](./hardware/comma.md).
- [Check vehicle compatibility](./cars/support.md).
- [Find car setup guides](./cars/all.md).
- [Install StarPilot](./software/starpilot.md).

## Shared work and project development

StarPilot builds on openpilot and FrogPilot. Features such as Always On Lateral,
Conditional Experimental Mode, themes, and Speed Limit Controller have shared project
history; their presence alone does not make them exclusive to StarPilot. The
[StarPilot project README](https://github.com/firestar5683/StarPilot#features) identifies
inherited features.

For questions about a feature on your car or software branch, use the
[StarPilot support channels](./ticketsystem.md). StarPilot remains driver assistance and
requires an attentive driver ready to take control.
