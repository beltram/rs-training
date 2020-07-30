## Combinator combination

* Yes, the combinators can be... combined !! Here's an example (link to the playground below)

```rust
fn at_least_two(number: u8) -> Option<String> {/* Omitted */ }
fn double_other_than_one(number: u8) -> Result<i32, String> {
    at_least_two(number)
// Transform the Option into a Result<String, String>
        .ok_or("Give a number greater than one".to_owned())
//Parse the inner Result value(if Ok) into i32.Return Result<i32, ParseIntError>
        .and_then(|it| it.parse::<i32>()
        .map_err(|err| err.to_string())) // Transform error type into String
        .map(|n| 2 * n) // Modify inner value and return Result<i32, String>
}
fn main() {
    match double_other_than_one(3) { // will print: 6
        Ok(n) => println!("{}", n),
        Err(err) => println!("Error: {}", err),
    }
}
```
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=5891f30482d463650fe72dcb1203bf62)