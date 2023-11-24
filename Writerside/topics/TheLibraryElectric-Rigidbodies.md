# Rigidbodies
Scripts involving rigidbodies

## FreezeRigidbodies

Freezes every rigidbody in the scene. Will ignore existing kinematic RBs, anything with [DoNotFreeze](https://github.com/CarrionAndOn/TheLibraryElectric/wiki/Markers#donotfreeze), and the rigmanager.
* `Freeze()`
* `Unfreeze()`

***

## GravityChamber

Must have any collider set as trigger attached.

Changes the gravity of any rigidbody in the area, leaving other rigidbodies outside of it unaffected.

The rig manager can be ignored if you choose to do so.