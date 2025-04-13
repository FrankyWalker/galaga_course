# Implementing Board Boundaries

Now that we understand how to control the terminal with Crossterm, let's create a method to display our game board with
visual boundaries.

## Your Task:

Create a public method called `display_board` in your `GameState` implementation that draws a border around your game
board.

### Requirements:

- The method should take a reference to `self` (`&self`).
- Position the cursor at the top-left corner of the terminal before drawing.
- Use `+` characters for corners, `-` for horizontal borders, and `|` for vertical borders.
- Include appropriate padding for visual clarity.

---

### Step-by-Step Guide:

**Step 0: Add the method signature and set up cursor positioning.**

```rust
pub fn display_board(&self) {
    execute!(stdout(), MoveTo(0, 0)).unwrap();

    // Step 1: Draw the top border of the board
    // We print some padding for centering, then a '+' for the corner,
    // followed by horizontal dashes '-', then another '+' for the other corner.
    print!("           +");
    for _ in 0..COLUMNS {
        print!("-");
    }
    println!("+           "); // End the line and finish the top border.

    // Step 2: Draw the board's content rows
    // For each row, draw a line that starts and ends with '|' (the side walls).
    // In between, fill with spaces (representing the empty board cells).
    for _ in 0..ROWS {
        print!("           |"); // Left border of the board.
        for _ in 0..COLUMNS {
            print!(" "); // Empty space inside the board.
        }
        println!("|           "); // Right border of the board and end of the line.
    }

    // Step 3: Draw the bottom border (same as the top border).
    print!("           +");
    for _ in 0..COLUMNS {
        print!("-");
    }
    println!("+           "); // Complete the bottom of the board.
}
```

---

### Why do we want a reference to `self` instead of `self` itself?

Think about ownership in Rust. If we took `self` instead of `&self`, what would happen to the `GameState` after this
method runs?

---

**Step 1:** Draw the top border.

- How would you draw a line with `+` at each end and `-` characters in between?
- Remember to use `COLUMNS` from our imported constants to determine the width.

**Step 2:** Draw the left and right borders.

- How would you draw vertical borders with `|` characters?
- The height should be determined by the `ROWS` constant.
- Don't forget to fill the space between borders with empty spaces.

**Step 3:** Draw the bottom border.

- This should match the top border pattern.

---

### Expected Result:

When completed, your board should display with a clear boundary like:
```
+---------+           
|         |           
|         |           
|         |           
+---------+
```