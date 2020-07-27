## integers euclidean division

```rust
let num: u8 = 5;
let quotient = num / 2; // shorthand
let remainder = num % 2; // shorthand
let is_even = num % 2 == 0;
let is_odd = num % 2 != 0;
let quotient = num.div_euclid(2);
let remainder = num.rem_euclid(2);
assert_eq!(2, quotient);
assert_eq!(1, remainder);
// impress your co-workers
let (quotient, remainder) = (num / 2, num % 2);
```