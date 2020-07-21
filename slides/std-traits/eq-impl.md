## [Eq](https://doc.rust-lang.org/std/cmp/trait.Eq.html), [PartialEq](https://doc.rust-lang.org/std/cmp/trait.PartialEq.html)

```rust
#[derive(Eq, PartialEq)]
struct Credential { login: String, password: String, }
// can be derived since all fields type impl Eq

struct Account { id: u32, description: String, }
impl Eq for Account {} // no implementation required
impl PartialEq for Account {
    // we want to narrow equality just to 'id' field
    fn eq(&self, other: &Self) -> bool { self.id == other.id }
}
```