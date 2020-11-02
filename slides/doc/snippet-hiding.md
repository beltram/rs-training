## hiding snippet elements

* start your code line with # to hide it (for clarity or walkthrough) - will still be compiled

```rust
/// First, we set `x` to five and `y` to six:
/// ```.
/// let x = 5;
/// ```.

/// Then, we print the sum of `x` and `y`:
/// ```.
/// # let x = 5; // will be hidden in HTML documentation
/// # let y = 6; // will be hidden too
/// println!("{}", x + y);
/// ```.
/// ```. is for escaping reveal.js ;) 
```

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html#hiding-portions-of-the-example)