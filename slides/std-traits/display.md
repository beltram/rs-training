## [Display](https://doc.rust-lang.org/std/fmt/trait.Display.html)

* similar to [Debug](https://doc.rust-lang.org/std/fmt/trait.Debug.html) but for explicit, custom printing
* struct implementing [Display](https://doc.rust-lang.org/std/fmt/trait.Display.html) can be used with '{}' formatter

```rust
use std::fmt::{Display, Formatter, Result};

struct Point { x: u8, y: u8 }
impl Display for Point {
    fn fmt(&self, f: &mut Formatter<'_>) -> Result {
        write!(f, "f({}) = {}", self.x, self.y)
    }
}
assert_eq!("f(3) = 9", format!("{}", Point { x: 3, y: 9 }));
```