## if

* no () surrounding condition 'if a == 0'
* mandatory {} 'if a == 0 {}'

```rust
if a == 0 {
    println!("0");
} else if a == 1 {
    println!("1");
} else {
    println!("?");
}
// () are tolerated but not encouraged when not required
if (a == 0) { println!("0"); }
```

[📒](https://doc.rust-lang.org/1.7.0/book/if.html)