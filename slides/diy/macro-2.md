## Declarative macros
* uses `!` macro operator
* similar to `match` Rust pattern (based on matchers)
* allows variable parameter number
    
```rust
#[macro_export]
    macro_rules! min {
        ($numbers:expr) => {
            let numbers = ($numbers as Vec<i32>);
            println!("{} is the minimal value amongst the list {:?}", numbers.clone().get_minimal(), numbers);
        };
    }

fn main() {
  min!(vec![1, -12, 0]); 
  // prints "-12 is the minimal value amongst the list [1, -12, 0]"
}
```