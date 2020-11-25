### Note

```rust
# [cfg_attr(target_os = "linux", cfg_attr(feature = "multithreaded", some_other_attribute))
```

is equivalent to

```rust
# [cfg_attr(all(target_os = "linux", feature ="multithreaded"), some_other_attribute)]
```
