# Testing Branch

StarPilot was based off of openpilot v0.9.7.
It has always had the newest tunes and driving models, 
but the older openpilot base version did not support newer hardware features 
like the C4 and dashcam audio.

The new testing branch updates to the latest Openpilot v0.10.0, 
which means it supports C3, C3X, **and C4**.
It can be installed using [the normal install process, but use this link](./starpilot.md):
`firestar5683/StarPilot-Development`. 
If already using StarPilot, you can use the branch switcher: `StarPilot-Development`.
Please beware long install times, it is a large update (due to AGNOS).

## Disclaimer

This is a testing branch. You should *expect* bugs and errors to occur. 
Please post issues in 
[the discord thread](https://discord.com/channels/1137853399715549214/1485152739368501410).

## New Features

* Full support for C3, C3X, C4.
* Dashcam audio recording
* Comma's new image pipeline optimizations.
