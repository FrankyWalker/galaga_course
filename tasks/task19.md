# Task19

In player.rs we are going to build out our struct `Player`. All of our
fields will be public. Use the names provided for each respective field
below. Your job is to figure out their types.

Create a field named `display_char` who's type will be used to represent
the player on the screen. Remember that this is a terminal-based game.

Create a field named `lives`. This is the number of lives the player has
remaining.

Create a field named `current_position`. HINT: use a `Option` type. Think
about which Type would make sense for the `Some` variant (we already have
this defined).

Create a field named `start_position`. HINT: I wonder if you could use the
same type here that was found in the `Some` variant from the previous
field?

Create a field named `death_timer`. This is the timer for respawning after
death.

Create a field named `key_reader`. This is an asynchronous key handler. It 
allows us to handle keyboard input with blocking the rest of the program.

## OA


