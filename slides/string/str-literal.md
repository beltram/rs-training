## string literal

String literals are inlined within the executable.  
They are present in a read-only memory section once the program is executed.  
Of course they are immutable.  
They can be thought as constants.

```rust
let a_string_literal: &str = "Pascal" 
let a_string_literal: &'static str = "Pascal" // 'static lifetime is implicit
```

[📒](https://doc.rust-lang.org/1.7.0/book/strings.html)