## lifetime advanced

* inheritance: 'a : 'b implies 'a lives at least as long as 'b
* generics bounds: T : 'a implies T is valid at least during 'a

```rust
// inheritance, Parser will have to return a reference to input string slice
// when context is dropped, it does not want to loose input borrow
struct Context<'s> { input: &'s str }
struct Parser<'c, 's : 'c> {
    context: &'c Context<'s>
}

// generics bounds: T can be anything here e.g. String, &String
// we need to ensure that if T is &String, T is at least valid for 'a
// otherwise we would reference a reference that no longer exists
struct Mock<'a, T : 'a>(&'a T);
```

[📒](https://doc.rust-lang.org/1.30.0/book/second-edition/ch19-02-advanced-lifetimes.html)