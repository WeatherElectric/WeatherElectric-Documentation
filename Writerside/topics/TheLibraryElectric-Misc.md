# Misc
Misc scripts

## DestroyOnCollision

Destroys everything it touches, ignoring stuff with [DoNotDestroy](TheLibraryElectric-Markers.md#donotdestroy), map geometry, and the rig manager.

***

## DespawnPooledObject

Despawns the object the script is on safely. Must be on an object that's spawned via crates.
* `Despawn()`

***

## InvokeIfLibInstalled

Invokes an ultevent if the player has the code mod installed. Does nothing without the code mod. Useful if you want to disable an SDK primitive method of doing something if the player has this mod to do the cooler way.

***

## RandomAudioPlayer

Plays a random audio source in the array you provide.
* `PlayRandomSound()`

***

## SpawnCrateOnTriggerEnter

Spawns a crate at the position something enters the attached trigger col.

***

## SpawnOnTriggerEnter

Same as SpawnCrateOnTriggerEnter, but it just instantiates a prefab instead.

***

## TimescaleController

Sets the timescale of the game. Increments by the specified value. Cannot go to 0 or below.
* `ScaleTime()`
* `IncreaseTimeScale()`
* `DecreaseTimeScale()`

***

## UpdateTMP

Made specifically for a spawnable I was making. The TextMeshPro must be only a number. UpdateTMP will increase/decrease the number by the configured amount when the respective method is called.
* `IncreaseValue()`
* `DecreaseValue()`