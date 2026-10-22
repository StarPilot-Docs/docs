---
title: Cameras & Monitoring — V-ASM, PiP, Sentry, and Snapshots
description: Configure visual spot monitoring, the blind spot camera preview, Sentry, and camera snapshots in Galaxy.
---

# Cameras & Monitoring

In [Galaxy](../usage/galaxy.md), **Cameras & Monitoring** contains the blind spot camera preview (PiP), [Sentry](./sentry-mode.md), V-ASM spot monitoring, and a camera snapshot tool. Configure them while parked. For road-camera speed sign detection, see [Vision speed limits](./speed-limit-controller.md#vision-speed-limits).

## Camera Snapshot

On the main **Cameras & Monitoring** page, turn off the vehicle, choose **Cabin**, **Wide road**, or **Road**, then tap **Take snapshot**. Use **Clear** to remove the preview. These snapshots are temporary and are not saved as Sentry events.

## V-ASM: adjacent spot monitoring

V-ASM adds visual spot warnings alongside factory blind spot monitoring, where available. It does not confirm that a lane is clear or change vehicle controls. Always check mirrors and look over your shoulder before changing lanes.

**Why the window regions are required:** The cabin camera also sees the driver, pillars, and interior. V-ASM uses each region to crop and mask the matching side-window view before checking it for a vehicle. This tells the model which side to inspect and keeps unrelated parts of the image out of its input. At least one side must be marked before monitoring can be enabled; mark both sides if you want warnings on both.

1. In Galaxy, open **Cameras & Monitoring → V-ASM** while parked. Tap **Take new snapshot** to load the cabin camera image.
2. Select **Left** or **Right** for the *vehicle* side you want to mark. The preview is mirrored, so the vehicle's left appears on the left; Galaxy stores it as camera right. The vehicle's right appears on the right and is stored as camera left.
3. Tap around the visible side glass for that side, then repeat for the other side. Include the front and rear side windows and as much visible glass as practical. Leave out pillars, door frames, and interior; include a side mirror if visible through the glass. A B-pillar can be inside a continuous region if needed. Use **Undo** or **Clear** to fix points. Each region needs at least three points.
4. Tap **Save**, review the region, and confirm. Then turn on **Use visual spot monitoring** under the saved settings. A drawn region by itself does not enable warnings.

**Detection confidence** sets how strong the model's evidence must be (0.80–1.00). Raising it may reduce false alerts but miss vehicles. **Warning smoothing** (0.01–0.50 seconds) controls how quickly warnings change; raising it reduces flicker but delays changes. Start with the defaults and adjust only if you notice a problem. Changes to these settings require the vehicle to be parked.

The cabin snapshot stays in your browser and is not uploaded by the region editor. If a warning is missing or incorrect, you can [submit an edge case or read about the training data](https://github.com/prabhaavp/vasm-op).

## PiP: blind spot camera preview

**Blind Spot Camera and Preview** shows a close-up of a cabin side window on the driving screen. It can appear when you signal, when the car reports a blind spot warning, or when V-ASM reports a visual spot warning. It is a view for the driver, not a second detection model.

In Galaxy, open **Cameras & Monitoring → Blind Spot Camera and Preview** while parked. Take a cabin snapshot, choose **Left camera** or **Right camera**, and place its circular crop over the matching side window. Adjust **Crop size**, then **Save** and confirm. Turn on **Use blind spot camera** and choose **Show on turn signal**, **Show on blind spot warning**, or both. The warning option responds to factory blind spot warnings and to V-ASM warnings when V-ASM is configured and enabled. You can position the onroad camera views with the layout editor.

PiP's circular crop controls what appears on screen. V-ASM's window regions control what its model analyzes; configure them separately. PiP also needs a live cabin camera and a crop for the side being shown.

## Sentry: parked motion events

Open **Cameras & Monitoring → Sentry** for parked motion monitoring, saved events, and notifications. See the [Sentry Mode guide](./sentry-mode.md) for setup and event details.
