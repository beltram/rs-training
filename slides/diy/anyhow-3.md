## anyhow - throw error

```rust
fn check_answer(answer: String) -> anyhow::Result<u32> {
    let parsed_input = answer.trim_end();
    if parsed_input.len() == 6 {
        Ok(u32::from_str(parsed_input)?)
    } else {
        bail!("Input should be 6 character long")
    }
}
```
