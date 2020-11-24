## lifetime elision rules
* If there are multiple input lifetime positions, but one of them is &self or &mut self, the lifetime of self is assigned to all elided output lifetimes.
```rust
fn get_mut(&mut self) -> &mut T;                        // elided
fn get_mut<'a>(&'a mut self) -> &'a mut T;              // expanded

fn args<T: ToCStr>(&mut self, args: &[T]) -> &mut Command                  // elided
fn args<'a, 'b, T: ToCStr>(&'a mut self, args: &'b [T]) -> &'a mut Command // expanded
```
