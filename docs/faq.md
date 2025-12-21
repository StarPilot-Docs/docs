---
description: Frequently asked questions
---

# Frequently Asked Questions

Can't find an answer to your question? Post in 
[Discord](https://firestar.link/discord)

## Will installing openpilot void my warranty?

<https://comma.ai/support#will-installing-a-comma-device-void-my-warranty>

## Is the openpilot install reversible?

Yes. The openpilot hardware install is fully reversible. 
There are no car modifications, just custom harnesses that intercept at the existing harnesses.

When the comma USB-C is unplugged, your car can't tell the difference.

When the openpilot hardware (camera harnesses, pedal, ASCM, SASCM, SDSU, SDGM, etc.) are removed,
the car returns to stock.

## Will openpilot navigate on its own?

Navigate-on-openpilot support has been dropped by comma, 
so the models that support navigation are old and not recommended.
The feature will probably come back in the future, 
but keep in mind that with the limitations of most cars (especially steering torque) 
and openpilot hardware will never be like Tesla FSD.

## How do I clear the "LKAS Fault: Restart the car" error?

1. Turn your car off
2. Open your car door
3. Wait 2 minutes (you can close your door in the meantime)
4. Turn car on
5. Done. LKAS fault should have cleared.

## How do I avoid LKAS faults?

1. Never reboot, unplug, or power off the comma while your car is on. 
This **will** cause an LKAS fault.
2. Sometimes LKAS faults just happen. GM cars are very sensitive to the exact timing of the
steering messages. Heat can cause thermal expansion of the connectors, so if you see this
happen while driving, it is a good idea to reseat your openpilot connections: 
GM harness, OBD-C, pedal ethernet, etc. While reseating connectors, you can breathe hot air
into the connector (like fogging up a window, not blowing out a candle) to help clear dust
and dissipate static buildup.

## How do I clear the "Cruise Fault: Restart the car" error?

1. Turn car off
2. Open car door
3. Close car door
4. Turn car on
5. Wait 5 seconds
6. If your error is cleared, you are done. 
If the error is still present, go back to step 1. This can take 6 or more tries.

## How do I clear the "Controls Mismatch" error?

1. Turn car off
2. Wait 5 seconds
3. Turn car on

> [!NOTE] Remote Start Issues
> If you use remote start, to avoid issues, you should cycle the car off and then back on
> again after you get in. Otherwise, you might get the Controls Mismatch error.

## How do I upload logs for troubleshooting?

Logs are sent as routes. A route is a single drive (from car on to car off), 
with 1 minute segments. Log data contains all Openpilot data: video, comms, gps, etc.

> [!TIP] Logs never hurt, but are generally only needed when requested.

1. Navigate to [connect.comma.ai](https://connect.comma.ai)
2. Find the route your issue happened on and click on it. 
3. Click and drag the video slider over the section where the error happened.
The video will loop over this selected section, make sure the error is within. 
To undo your last selection, click the back arrow just above the video slider. 
Once you are happy with the segments selected, proceed to the next step.
4. Click `Files`, then next to `All logs`, click `(upload ## logs)`
5. Wait for data to be uploaded (you can check the progress using `Files` > `View Upload Queue`)
6. Click `More info`, then enable `Public access` and 
copy the Route info using the Copy button: ![Copy button](./assets/images/copy_clipboard.png)
7. Create a post in 
[#starpilot-troubleshooting](https://discord.com/channels/1137853399715549214/1415794830965080155). 
Be as descriptive as possible. Make sure to include software version and branch. 
Also include the approximate minute(s) in the route it happened. 
8. Paste the route info into the troubleshooting post. 
It contains the video and GPS data for your route, so if you'd rather not post it publicly, 
send it in DM to @firestar4430 and/or whomever is helping you 
(including a link to the troubleshooting post is helpful for context).

> [!TIP] Ending a route log early
> To make it easier to find the error, you can force the log to end early using:
> Settings > Utilities > Force offroad. This will make sure the error is near the end of
> the log. 

## What is redneck ACC (aka CC Long)?

This feature emulates a very basic ACC system 
by using the built-in cruise control system and then 
spamming virtual presses of the + and - buttons to control speed. 

Redneck ACC is able to handle small speed variations while following a lead on the highway. 
However, it is unable to change speed fast enough to 
handle slowing or stopped leads or operate below 24 mph (due to GM limitations),
so you will be experiencing a small fraction of what openpilot is capable of.
It is also quite jerky.

Do not expect it to stop for cars or react quickly. As always, be ready to intervene.

## I'm stuck on the boot logo screen. How do I fix it?

1. Unplug the device
2. Wait 60 seconds
3. Plug it back in
4. Tap the center of the screen over and over until the reset prompt comes up
5. Reset 
6. Reinstall [your desired version](./software/starpilot.md)
7. If this happens again, go back to step 1 and reinstall from `firestar.link/saveme`
and then swap to your intended branch (or uninstall and install your intended fork).

## How do I fix "Process Not Running dmonitoringmodeld"?

This occurs on upstream FrogPilot on relatively new comma devices (after September 2025)
as a result of upstream comma provisioning changes. Installing StarPilot will make the
device appear similar to before the provisioning changes. A single install of StarPilot will
fix it so you can go back to FrogPilot after.

1. Uninstall FrogPilot (Settings > Software > Uninstall)
2. Install StarPilot from `firestar.link/trx`
3. If you are staying on StarPilot, 
change to your desired branch in the Software tab and stop here. 
Otherwise, proceed.
4. Uninstall StarPilot
5. Reinstall FrogPilot

## How do I fix the "Propulsion Power Reduced" Error on my dash and regen not working? (for Bolts with Comma Pedal)

Your Bolt may have had a momentary issue communicating with the throttle pedal,
causing it to enter a limp mode. 
To clear any potential thermal expansion shifting or static buildup issues:

1. Turn off the car.
2. Unplug all connectors for the Comma Pedal.
3. Breathe hot "sultry" air into the connector ends.
This includes the two connectors coming out of the Comma Pedal box and the car side (if possible). 
This is hot breath like fogging up a window, not blowing out a candle.
4. Re-connect all connectors. 

If the issue still presents, post in the troubleshooting thread.

## How do I fix the "CAN bus disconnected" Error?

Openpilot had an issue communicating on the CAN bus. 
Reseat (unplug and plug back in) all of your openpilot connections 
(harnesses, OBD-C, pedal, etc).
