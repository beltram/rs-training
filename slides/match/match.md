## match

* match is an expression
* match arms must be exhaustive (cover all possibilities for the VALUE)
* _ can be used as PATTERN for default value (cannot create any binding though)
* An arm can't be unreacheable (after _ for example)
* match/if let/ while let take mainly [refutable](https://doc.rust-lang.org/book/ch18-02-refutability.html) patterns

```rust
match VALUE {
    PATTERN => EXPRESSION,
    PATTERN => EXPRESSION,
    PATTERN => EXPRESSION,
}
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#match-arms)