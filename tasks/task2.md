# Creating a game_state module

Create another file within the `src` directory called `game_state.rs`.

We don't write all of our code in `main.rs` because it would be overwhelming.
It's preferred to separate out the major logic of the codebase into
separate files, and then tie said logic into `main`. These separate files
are called modules.

This means, surprisingly, that while the total LoC (lines of code) could be
1000+ across the codebase, `main.rs` would be succinct at ~30.
