# Openpilot Operation

## Basic Operation

1. Pay attention at all times. You are responsible for your vehicle's operation.
2. You can manually override or disengage openpilot at any time. 
Steering, throttle, and brakes can be used at any time.
3. With Always on Lateral (AOL) - lane centering stays active at all times, 
even when Cruise Control (CC) is disengaged or pressing throttle/brake pedal. 
This does not change #2, you can always override it by manually steering.
To enable, turn the CC system on. To disable, turn CC system off.
4. To engage openpilot (ie. to make it control your speed), 
engage your CC system as normal by pressing SET/-. 
5. To disengage openpilot, it should be the same as your CC system. 
Press CC cancel or hit the brakes. GM Volts/Bolts can use the regen paddle.
6. To adjust openpilot max speed, use the CC +/- buttons. 
Depending on the car, your car's dash may not reflect the max speed, 
so instead use the openpilot UI's max speed shown.

## UI Basics

### Border Colors

1. None - openpilot is not engaged
2. Blue - openpilot is controlling only steering (AOL)
3. Green - openpilot is engaged
4. Grey - openpilot is engaged, but overridden (manually steering or pressing throttle pedal)
5. Orange - openpilot is engaged, [CEM](#conditional-experimental-mode) is active
6. Red - openpilot is engaged, personality set to Traffic Mode

### Max Speed

Your max speed is shown in the top left of the UI.

## Speed Limit Controller 

The Speed Limit Controller (SLC) will use map data from [Open Street Map (OSM)](https://openstreetmap.org) 
to limit your max speed based upon speed limit data for your vehicle location.

Speed limit for your current location is shown below your max speed. 
The active +offset shown is how far above the speed limit it will allow.
Offsets are configurable in settings.

If your max speed is *red*, SLC is limiting the speed to the speed limit + offset.

If your max speed is *orange*, your max speed is still active but approaching the SLC limit.

### Submitting New Speed Limits

If you see an incorrect or missing speed limit, go to OSM and submit an edit. 
Your openpilot speed limit data will update in about a week.

## Curve Speed Controller ![curve speed controller icon](../assets/images/curve_speed.png){: style="height:50px;width:50px"} 

The Curve Speed Controller (CSC) will limit your max speed in order to match how you take curves.
If you see the curve speed icon next to your max speed, 
CSC is overriding your max speed to the speed shown. 

If you think it is going too fast or slow for the curve, 
manually speed up or slow down by overriding throttle/brake 
and it will learn to match that speed over time.

## Experimental Mode

Normal openpilot operation is known as *chill mode*.

Experimental mode, also known as end-to-end longitudinal (e2e long), 
gives the driving model full control of the gas/brake. 
It is not recommended at the moment. 
It may brake or accelerate erratically.

One day, driving models will be good enough to stay in experimental mode full time, 
but for now we recommend keeping it disabled.

## Conditional Experimental Mode 

Conditional Experimental Mode (CEM) automatically switches into experimental mode 
under certain conditions, like approaching a traffic light or stop sign. 
Experimental mode can behave strangely at times, 
so we conditionally swap into it for conditions we know the driving model is better at.

The condition that caused the mode swap is indicated by a widget. 

### CEM Widgets and Meaning

* Couch - Chill/normal mode
* Traffic Light - Traffic lights or stop signs
* Car - (Slower or stopped) lead car
* Speedometer - CEM activated by being below speed threshold
* Steering wheel - Turn signal is on, speed is below threshold, and no detected lane
* Map - Navigation
