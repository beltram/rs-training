## Procedural macros
* custom derive macros

Generate additional code for an attribute (struct or enum)

```rust
#[derive(Serialize, Deserialize, Debug, Eq, PartialEq)]
pub struct User{
  // attributes
}
```
* attribute-like macros

Allows to add new attribute(s) to an item (applicable to functions)

```rust
#[route(GET, "/")]
fn index() {
  // implementation
}
```