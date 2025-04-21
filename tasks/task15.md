# Task15

Our game needs some way to simulate the passage of time. A "tick" (like
a clock, get it?) is a way to do just that.

Here's the problem:

/some_game/src/main.rs

```rust
fn main() {
    loop {
        enemy_movement();
        player_movement();
        some_function();
    }
}
```

Games are run in loops, like ours. But if you were to execute `main` above,
everything would happen way too quick. Like if in `enemy_movement` your 
algorithm had the enemy chase the player, he'd reach you instantly, becaus
e CPU's compute quickly! The solution is to implement a tick system. Then
the Dev could say, "each time the loop happens above, increment a counter
by one, when this counter reaches some interval X, `enemy_movement` will
execute. The counter will then be reset back to zero and it will start
over again. Ticks are also a way to coordinate actions across your codebase.

## TODO

In structs.rs, create a method named `tick` to the Timer impl block. The 
input parameter (hint: there is only one [remember ownership]) is for you
to decide. This method should return a `bool`. 

Each time this method is invoked, `current_time` shall be incremented by
`1`. If `current_time` reaches or exceeds `interval`, `current_time` shall
be reset to `0`. When this happens, `true` shall be returned. Otherwise,
`false` shall be returned.

## OA

Extra Credit: why does the reference to self in the input parameter above
need to be mutable?
