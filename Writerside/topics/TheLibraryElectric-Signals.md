# Signals
Signal scripts

## SendSignal

Invokes an ultevent across any object in the scene with [RecieveSignal](#recievesignal).

The activation key must be the same.

If the sender's key is "key1" and the receiver's key is "key1", it will invoke, but it will ignore any receivers that have a different key from "key1".

If many objects have "key1", they will all have their ultevents invoked.
* `Broadcast()`

## RecieveSignal

The receiver, holds the ultevent.

Set the ultevent to do whatever, and set the key to what your sender's key is.

***

## SignalTrigger

Triggers an ultevent once an object with the same key enters the trigger.

## SignalTriggerer

Triggers SignalTrigger if the keys match