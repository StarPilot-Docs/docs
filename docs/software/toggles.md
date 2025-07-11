—
description: How to configure your settings for the best experience
—

# Configure Toggles & Settings

WIP

## Toggles

Most toggles here are up to you.

!!! note “ACC Bolts Only”
    
    Enable “openpilot Longitudinal Control (alpha)”. This will use the smoother, tuned experience vs. the Bolt’s stock ACC. It does not disable automatic emergency braking.
    
## FrogPilot Settings

In general, FrogPilot settings should remain between fork installs and branch switches

There are multiple tuning levels in the FrogPilot settings - these will enable or disable more advanced tuning parameters.

For best results on StarPilot, you’ll need to use the **Advanced** level. 

!!! note

    To learn more about ay setting, tap the title to see a description
    
### Vehicle Controls

1. Select your car model.
2. Disable **Automatic Fingerprint Detection**.
3. Under **General Motors Toggles** DO NOT enable FrogsGoMoo’s experimental longitudinal tune or the Stop and Go hack. DO enable Smoothen Pedal Response While Going Downhill/Uphill.

??? note “Fingerprinting Info”

    Fingerprinting is inconsistent on GM vehicles at the moment. As such, sometimes ACC bolts decide to fingerprint as Non-ACC which causes fun issues such as… not having Gas/Brake. So to be sure, it’s just always best to manually fingerprint.

### Alerts and Sounds
These are optional changes. Some popular changes include:

* Under **Alert Volume Controller**, you can adjust or mute the disengage and engage sounds. We DON’T recommend changing the volume of any important alerts. 
* Under **Custom Alerts**, you can enable the Green Light Alert and Lead Departing Alert to get gentle nudges when a traffic light has turned green or the car in front of you has started moving.

### Driving Controls

**Additional Organization In Progress**

Under Driving Model, turn ON “Automatically download and update models”.

!!! warning

    This is a departure from previous advice - we used to advise against this due to the potential for incomplete models. But with the new tinygrad model switcher, having this on helps ensure all pieces of the model have been downloaded correctly.

!!! note

    For more info on driving models, see the [driving models](/software/models) page. 
    
  