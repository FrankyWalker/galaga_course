# Task13

In structs.rs, add two fields to the struct `Timer`, `current_time` and `interval`.
They should both be type u64.

`current_time` is a counter tracking the elapsed "ticks" since the last
interval reset, and interval is the threshold value at which `current_time`
should trigger and reset.

But what is a tick system? It's basically a timing mechaninsm to coordinate 
when events within the game happen, like how often our game state updates,
or more advanced things that OpenGalaga won't touch on like animation
frame timing.

## OA

