# Driving Model

The driving model is the "brains" behind openpilot. 
It processes video and outputs the desired steering and acceleration/braking.

Model preferences are personal; 
they can vary based upon vehicle, region, environment, and preferences.
This page is just a guide -- try a few models and search for feedback in the Discord.

> [!TIP]
> Models are released often, so this page can go out of date quickly.
> Discord will generally have the most up to date info.
> This page was last updated on: {{ git_revision_date_localized }}

## Current Recommendation(s)

* **Dark Souls v2**: The current favorite and default in upstream openpilot.

## Previous Favorites (newest to oldest)

Older models that aren't completely out of date yet. 

* Plan Plus (1 or 2)
    * This model adds 'Recovery Power' which adds a centering ability to the model.
    * Make sure to start with 'Recovery Power' at 0.6 if in a GM vehicle and adjust from there.
* Dark Souls
* Cool Green Watermelon
* Green Watermelon v8
* Green Watermelon v7
* The Cool People v3
* Firehose
