## anyhow - catch error

```rust
fn get_answer(prompt: &str) -> anyhow::Result<u32> {
    print!("{}: ", prompt.to_title_case());
    let _r = stdout().flush();

    let mut input = String::new();
    stdin().read_line(&mut input)
        .context(format!("Error while reading: '{}'", prompt))?;

    check_answer(input)
}
```

Reminder about `?` operator [📒](https://doc.rust-lang.org/edition-guide/rust-2018/error-handling-and-panics/the-question-mark-operator-for-easier-error-handling.html)