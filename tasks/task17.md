# Task17

In player.rs, import these items:
```rust
use console::Key;
use crate::structs::{ROWS, COLUMNS, Cords, Timer};
use std::process::exit;
use console::Term;
```

Just to make sure we're all on the same page, let's quickly look at 
`use console::Key`. We use the `use` keyword to bring into scope items that
we want to use in the file we're working on. So in this case, we're 
importing `Key` from the external crate `console`. The `::` is called the Scope 
Resolution Operator. This means that in the body of our code, we can simply
type something like 

`let key = Key::Char('a');`

instead of

`let key = console::Key::Char('a');`

The crate `console` contains lots of different Types, you can see them 
here:

https://docs.rs/console/latest/console/

You see how we typed individually imported both `Key` and `Term` from above?
We could've also typed

`use console::{Key, Term};`

The reason we only import specific items from crates, and not the entire
crate itself is for clarity (other Devs know what we're using w/o searching),
and naming conflicts -- different crates sometimes use the same names for
their own defined Types. It's also more idiomatic.
