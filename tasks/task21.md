# Task 21

In player.rs, create a public async method inside the Player impl block. This 
asynchronous function is responsible for handling key inputs and performing actions
based on the key pressed. It is useful for controlling movement on a grid or 
similar coordinate-based structure.

What should this method take as an input parameter? It's return value should be 
the Option enum wrapping the `Cords` type.

If `self.current_position` contains a valid `Cords` (x,y):

- `ArrowLeft`: Moves to the left if `y > 0`.
- `ArrowRight`: Moves to the right if `y < COLUMNS - 1` (staying within bounds).
- `ArrowUp`: Returns a new `Cords` with the x-coordinate decremented `(x - 1)`.
- `CtrlC`: Exits the program immediately using `std::process::exit(0)`.
- Any other key is ignored.
- If `self.current_position` is `None`, the function simply returns `None`.

## OA
