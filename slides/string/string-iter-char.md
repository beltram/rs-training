## iterating over String's chars

* recommended approach
* use '.chars()' to get an 'Iterator<char>'

```rust
let french_hawk = String::from("épervier");
assert_eq!(Some('é'), french_hawk.chars().next());
assert_eq!(Some('\u{00e9}'), french_hawk.chars().next());
//               -------- raw unicode notation
for c /*:char*/ in french_hawk.chars() {
    print!("_{}_", c);
}
```
