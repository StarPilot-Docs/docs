---
description: How to configure your settings for the best experience
---

# Configure Toggles & Settings

WIP

## Toggles

Most toggles here are up to you.

<!-- Pulled the below note from the old guide - not sure where this setting is? -->

!!! note "ACC Bolts Only"

	Enable "openpilot Longitudinal Control (alpha)". This will use the smoother, tuned experience vs. the Bolt’s stock ACC. It does not disable automatic emergency braking.
    
## FrogPilot Settings

In general, FrogPilot settings should remain between fork installs and branch switches.

!!! note "TL;DR?"

    Just look for all the ==blue highlights== - they will tell you any settings you need to turn off or on for best experience. 

## Tuning Level

There are multiple tuning levels in the FrogPilot settings - these will enable or disable more advanced tuning parameters.

For best results on StarPilot, you’ll need to ==use the **Advanced** tuning level==. 

!!! note

    To learn more about any setting, tap the title to see a description

    
## Alerts and Sounds

These are optional changes. Some popular changes include:

* Under **Alert Volume Control**, you can adjust or mute the disengage and engage sounds. We DON’T recommend changing the volume of any important alerts.
* Under **FrogPilot Alerts**, you can enable the Green Light Alert and Lead Departing Alert to get gentle nudges when a traffic light has turned green or the car in front of you has started moving.


## Driving Controls

### Driving Model

* Automatically download and update models: ==Turn On==

!!! warning

    This is a departure from previous advice - we used to advise against this due to the potential for incomplete models. But with the new tinygrad model switcher, having this on helps ensure all pieces of the model have been downloaded correctly.

Full info on models coming soon. For now, try the following:

* **WD-40**: A smooth, but outdated experience. It'll be like 75% good for lateral and longitudinal control.
* ==**Vikander**==: A custom model by the venerable chubbs. Great long, decent lat. Some users experience bad oscillations, but it varies by environment, so try it out! 
* **TR Models** "Tomb Raider" models. There's always a new version, TRX is decent, try the highest TR## available.
* **Simple Plan (SP)**: A newer model than the above, still testing - seems to work pretty well overall!
    

### Gas / Brake

#### Conditional Experimental Mode: ==Turn On==

These settings control Conditional Experimental Mode, often called "CEM". Experimental Mode (vs "Chill Mode") is not yet good enough to handle all driving. But it can handle traffic lights & stop signs, and is better in some situations. So we automatically enable it in certain conditions where it is better than Chill.

Experimental Mode has a tendency to slow down/speed up weirdly, and overall just behave strangely, so we recommend conditionally enabling it only when necessary. 

* **Curve Detected Ahead:** Can be useful if you regularly take tight corners above the speed limit. Activates when a tight curve is detected. Most leave this off. Likely to be superseded by a fancy new curve speed control FrogsGoMoo is working on.
* **Lead Detected Ahead:** ==Non-ACC - Turn on both Slower Lead and Stopped Lead==, to help the model better slow when using VOACC (Visual Only ACC). 
* **Navigation Data:** Recommend leaving off.
* **openpilot Wants to Stop In:** Helps with slowing to a stop at lights, in traffic, etc. ==Default is 8 seconds==. Increase this number if your car is not slowing down in time for leads/lights. Decrease this number if you're getting lots of false activations and the car is going in and out of CEM when it shouldn't.
* **Status Widget:** Up to you. Recommend leaving on. Shows an icon that displays if CEM is active, and if so, why.


#### Curve Speed Control: Personal Preference

Relatively privative currently. Slows down for curves. Advanced CSC coming soon. 


#### Customize Driving Personalities: Personal Preference

Allows you to enable or disable certain personalities.

Manage lets you set the follow distance to your preference.

These have been tuned by firestar - if you wish to tune how they react, you can unlock additional settings by switching to the *developer* tuning level. Be careful though! 


#### Longitudinal Tuning: ==Turn On==

* **Acceleration Profile:** ==Sport==
* **Deceleration Profile:** ==Eco==
* **Human Like Accel/Leads:** These do... things? This will change how the model acts. Sometimes quite significantly. Varies model to model. Test with on and off. 
* **Taco Bell Run:** Just leave taco bell run stuff off.

!!! note "Hate a model?"

    Model trying to drive you into the back of leads? Model leaving a gap of 200 certified football fields? Try turning on or off the "Human Like" settings -  they often change quite a bit about a model's behavior.
    
    
#### Quality of Life: ==Turn On==

WIP - Sorry... still working. For now, see [firestar.link/bolt](http://firestar.link/bolt) for the rest. Thanks ayboa!

### Steering

## Navigation

## System Management

## Theme and Appearance

### Appearance

### Theme
    
## Vehicle Controls

### Vehicle Settings
    
1. Select your car model.
2. Disable **Automatic Fingerprint Detection**.
3. Under **General Motors Toggles** DO NOT enable FrogsGoMoo’s experimental longitudinal tune or the Stop and Go hack. DO enable Smoothen Pedal Response While Going Downhill/Uphill.

??? note "Fingerprinting Info"

    Fingerprinting is inconsistent on GM vehicles at the moment. As such, sometimes ACC bolts decide to fingerprint as Non-ACC which causes fun issues such as… not having Gas/Brake. So to be sure, it’s just always best to manually fingerprint.
    
### Wheel Controls