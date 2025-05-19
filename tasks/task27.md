# Task 27

In player.rs, create a constructor for the `KeyReader` structure. It should specifically return a `KeyReader` instance, which is more
descriptive than using Self in this case, as the purpose of the structure is clearly defined and unchanging.

This method spawns a new asynchronous task using `tokio::spawn`. The task invokes the `await_key_press` method, which
listens for key presses.

## OA
