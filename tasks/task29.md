# Task 29

In player.rs, create the method `read_key` inside the `KeyReader` struct.

This method reads a key asynchronously if the task has been completed.

It accomplishes this if the asynchronous task (`jh`) is finished. If the task
is finished, it retrieves the result of the task (a `Key`), spawns a new task
for awaiting the next key press, and returns the retrieved key in the `Option` type.
If the task is not finished, it returns `None`.

To be clear, this method should either return `Some(key)` (if the key press task has completed) or `None`
(if the task is still in progress).

## OA 
