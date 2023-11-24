# Water
Water-related scripts.

## DrowningManager

If the player is in the trigger for a specified amount of time, the player will start taking a set percentage of their health as damage at a set interval.

**Recommended values:**
* `30` time until drowning
* `1` damage interval
* `0.1` damage percent

***

## SwimmingController

Lets the player swim with their hands, adding force in the direction they look when their hands move at a specific velocity

**Recommended values:**
* `10` min velocity
* `100` velocity multiplier

***

## WaterZone

A zone of "water". Objects with a mass higher than the set midzone will sink, while objects with a mass lower than the set midzone will float. The player usually always floats unless your midzone is really low.

**Recommended values:**
* `50` midzone
* `1` buoyancy multiplier
* `0.98` dampening
* Midpoint sink enabled

## IgnoreRigidbody

Makes WaterZone ignore the rigidbody this component is attached to, making it immune to water physics.