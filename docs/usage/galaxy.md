---
title: Galaxy — Remote Settings & Device Management
description: Use Galaxy, the StarPilot web interface, to pair your comma device, manage settings from your phone, debug issues, and view recordings.
---

# Galaxy

Galaxy is StarPilot's web UI for configuring settings, debugging, and viewing recordings. 
It can be used from your phone on the same local network or remotely.
It is free and will remain free for as long as possible.

## Pairing

Once your device is paired, your device will remain paired until unpaired.

1. On your comma device, open Settings > Device > Galaxy (Pair).
2. Enter your desired passcode.
3. Scan the QR code that appears. Save this URL to access the galaxy in the future.

> [!IMPORTANT] Save the URL from the QR code
> The QR code's URL is unique to your device. Save it for future use.
> It will also change if you re-pair.

> [!IMPORTANT] Be patient when first pairing.
> It may take few minutes for the tunnel between your device and the galaxy server to establish.

> [!TIP] Multiple Comma Devices
> If you have multiple comma devices and you want to switch between them, 
> bookmark the auth URLs for each one (the URL that results from scanning the QR code).
> Open the URL of the desired comma each time you need to switch.

## Unpairing

1. On your comma device, open Settings > Device > Galaxy (Unpair).
2. Your device should now be unpaired.

## Local Access

For the tech savvy, galaxy is reachable locally at comma-ip:8082 if you wish to avoid the relay server.

## Features

The most notable features include:

- **Home & Routes:** View drive statistics, recordings, and downloads.
- **Toggles & Vehicle Controls:** Search and change settings, choose Auto or manual vehicle detection, and configure [Vision Speed Limit Detection](../exclusive/speed-limit-controller.md).
- **Models:** Download and switch driving models, compose Model Laboratory pairs, and set up Jetlink.
- **Colors & Layout:** Customize onroad layouts and themes.
- **Tuning & Plots:** Tune lateral behavior with FLM and inspect live control plots.
- **Navigation & Maps:** Set destinations and compare routes. See the [Navigation guide](../exclusive/navigation.md).
- **Android Auto:** Show the driving view on your car’s screen. See the [Android Auto guide](./android-auto.md).
- **Cameras & Monitoring:** Manage [Sentry Mode](../exclusive/sentry-mode.md) and V-ASM spot monitoring.
- **Bluetooth:** Pair controllers, keyboards, and other accessories.
- **Logs & Diagnostics:** Review non-default settings, error logs, tmux, temporary drive state, and help links.
- **System Tools:** Check for and install StarPilot updates.
