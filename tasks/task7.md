# Add a hash map dependency to the top of game_state.rs file.

1. The type HashMap is included in the Standard Library, but is not included
in the Prelude.


2. If something is included in the SL (Standard Library), we don't need to pull in an external
crate, it's found locally (but still needs to be imported into whatever
file you are working with).

3. Separately, the Prelude includes common things like the Option type or
basic traits like Clone. We don't need to import things that are found
in the Prelude.
---
OA:
```rust
use std::collections::HashMap;
```