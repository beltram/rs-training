## match

* match is an expression i.e. may have a result
* match arms must be exhaustive (cover all possible values)
* '_' can be used as PATTERN for default value (cannot create any binding though)
* an arm can't be unreachable (after _ for example)
* match/if let/while take mainly [refutable](https://doc.rust-lang.org/book/ch18-02-refutability.html) patterns

```rust
match VALUE {
    PATTERN => EXPRESSION,
    PATTERN => EXPRESSION,
    PATTERN => EXPRESSION,
}
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#match-arms)