# Task12

In structs.rs, make a public tuple struct named `Cords` with two fields,
each of type pub usize.

Note that you've probably only been exposed to Named-Field Structs so far
like:

```rust
pub struct Sandwich {
		pub name: String,
		pub price: f32,
		pub is_toasted: bool,
}
```

There are multiple types of structs. Read about them here:

[Rust Book -- Structs](https://doc.rust-lang.org/book/ch05-01-defining-structs.html)

Create a derive attribute to implement Clone, Copy, Eq, Hash, and PartialEq
on `Cords`.

Create a public struct called `Timer` and a impl block for `Timer`.

## OA: