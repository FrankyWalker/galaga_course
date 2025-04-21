# Game State Implementation

In `game_state.rs`, we implement the main game loop with an asynchronous function that controls the game flow:

```rust
pub async fn start_game(&mut self) -> Result<(), String> {
    loop {
        thread::sleep(Duration::from_millis(10));
        self.display_board();
    }
    Ok(())
}
```

## Explanation

This function implements the main game logic that runs continuously until the game ends:

- It's declared as `async` to support asynchronous operations
- It takes a mutable reference to `self` (`&mut self`) to modify the game state
- It returns a `Result<(), String>` where:
    - `Ok(())` represents successful completion (with the Unit type `()`)
    - `Err(String)` represents failure with an error message

The function uses a `loop` control-flow construct to run code continuously. Within the loop:
1. The thread sleeps for 10 milliseconds using `thread::sleep(Duration::from_millis(10))`
2. The game board is displayed using `self.display_board()`

Note that this implementation creates an infinite loop that will never reach the `Ok(())` statement. In a complete implementation, you would need to add a condition to break out of the loop when the game should end.

## Asynchronous Programming

In synchronous code, operations happen sequentially (Function1 → Function2 → Function3). If Function2 takes time to complete, the entire program must wait.

Asynchronous code allows non-blocking operations. Instead of Function2 holding up the program, it can run when ready (e.g., when player input is received) while the program continues with other functions.

This is particularly important in games where you need to maintain continuous execution for animations, enemy movements, and other game mechanics regardless of user input timing.

## Task TODO

In main.rs, import the `game_state` module. Import the GameState struct from the
`game_state` module with the use keyword.

https://doc.rust-lang.org/book/ch07-04-bringing-paths-into-scope-with-the-use-keyword.html

Make the main function async, and have it return a Result type with the Ok var
iant as a unit type and Err variant as a String.

Why would we have main() return a Result type? Up until now, all of our 
programs looked like this:

```fn main() {
//your program
}
```

Copy this attribute on top of main()

`#[tokio::main]`

For now, just understand that this attribute is supplied by the Tokio li
brary. It makes your async code signinifcantly simpler by allowing you 
not having to manually set up a runtime environment for async code.

Now that you have imported GameState into main.rs, you have acess to it's
methods and associated functions. 

Declare a mutable var called game and bind it to GameState's new() const
ructor function.

Call the `start_game` method from the GameState implementation onto game. 

Attach the await keyword after `start_game()` using this syntax: 

`.await?;`

While .await looks like a method because of the . it's actually a keyword
used in async code. You can read more about the await keyword in the link
below, but it's ok if at this point you just understand that it's used with 
async code.

https://doc.rust-lang.org/std/keyword.await.html

Finally, within main() finish the function with the Ok variant containing 
the unit type.

## OA:

