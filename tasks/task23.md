# Task 23
In player.rs, create a public method named `handle_collision`
inside the Player impl block.

This method handles a collision by decrementing the player's 
lives. If the player has no lives left after the collision, the
method should return the `None` variant of the `Option` enum. Otherwise,
it resets the player's current position and returns the remaining
lives. If the player does have lives left, it should return the
number of them as a `u8` in the `Some` variant.

## OA
