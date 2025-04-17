# Create three constants at the top of your structs.rs file.o


1. The first constant will be called SIZE and will be an usize bound to 10.

2. The second constant will be called ROWS and will be an usize bound to SIZE.

3. The third constant will be called COLUMNS, will be an usize and equal to SIZE * 2.

NOTE: the pub keyword allows us to use code between modules.

Game board dimensions that go inside struct.rs

---
## OA 
```rust
pub const SIZE: usize = 10;
pub const ROWS: usize = SIZE;
pub const COLUMNS: usize = SIZE * 2;
```
