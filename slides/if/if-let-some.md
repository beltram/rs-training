## if let Some

```rust
// destructuring Option
let balance: Option<u8> = Some(10);
if let Some(amount) = balance {
    println!("I have {}€", amount);
} else { println!("I have 0€") }
// destructuring Result
let tryout: Result<u32, ()> = Ok(200);
if let Ok(http_status) = tryout {
    println!("http status response {}", http_status);
}
```

[📒](https://doc.rust-lang.org/stable/rust-by-example/flow_control/if_let.html)