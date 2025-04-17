# Creating a publicly available function named new

1. Within the impl block for GameState, create a publicly available function
named new. This function will not accept any input parameters, and will
return the type GameState.
---
## OA:
```rust
impl GameState {
	pub fn new() -> GameState { 
		GameState {}
	}
}
```
