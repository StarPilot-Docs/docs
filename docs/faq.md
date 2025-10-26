---
description: Frequently asked questions
---

# Frequently Asked Questions

## LKAS Fault

How do I clear the "LKAS Fault: Restart the car" error?

1. Turn your car off
2. Open your car door
3. Wait 2 minutes (you can close your door in the meantime)
4. Turn car on
5. Done. LKAS fault should have cleared.

How to avoid LKAS faults?

1. Never reboot, unplug, or power off the comma while your car is on. 
This **will** cause an LKAS fault.
2. Sometimes LKAS faults just happen. GM cars are very sensitive to the exact timing of the
steering messages. Heat can cause thermal expansion of the connectors, so if you see this
happen while driving, it is a good idea to reseat your openpilot connections: 
GM harness, OBD-C, pedal ethernet, etc. While reseating connectors, you can breathe hot air
into the connector (like fogging up a window, not blowing out a candle) to help clear dust
and dissipate static buildup.

## Cruise Fault

How do I clear the "Cruise Fault: Restart the car" error?

1. Turn car off
2. Open car door
3. Close car door
4. Turn car on
5. Wait 5 seconds
6. If your error is cleared, you are done. 
If the error is still present, go back to step 1. This can take 6 or more tries.

## Controls Mismatch

How do I clear the "Controls Mismatch" error?

1. Turn car off
2. Wait 5 seconds
3. Turn car on

## Upload Route Logs

How do I upload route logs for troubleshooting?

> [!TIP] Logs never hurt, but are generally only needed when requested.

1. Navigate to [connect.comma.ai](https://connect.comma.ai)
2. Find the route your issue happened on and click on it. 
3. Click and drag the video slider over the section where the error happened.
The video will loop over this selected section, make sure the error is within. 
To undo your last selection, click the back arrow just above the video slider.
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
