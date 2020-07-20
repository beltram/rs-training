## closure

* aka lambda in jvm languages
* anonymous function with arguments coming from enclosing scope

```rust
let no_arg = || 1;
let single_line = |it: i32| it + 1;
let multi_line = |it: i32| {
    println!("adding 1 to {}", it);
    it + 1
};
// closure's type is a function pointer
let anonymous_fn_pointer: fn(i32) -> i32 = |it: i32| it + 1;
// return type is generally inferred. You generally don't have to write this
let explicit_return_type = |it: i32| -> i32 { it + 1 };
let multi_arg = |a: i32, b: i32| a + b;
// usage
let three = single_line(2);
let eleven = multi_arg(6, 5);
```

[📒](https://doc.rust-lang.org/1.17.0/book/closures.html)