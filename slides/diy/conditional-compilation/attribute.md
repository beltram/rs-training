##cfg attribute

```rustc
#[cfg(all(unix, target_pointer_width = "32"))]
fn on_32bit_unix() {
  // ...
}
```

## cfg_attr
to include attributes depending on configuration
 
```rustc
#[cfg_attr(target_os = "linux", path = "linux.rs")]
#[cfg_attr(windows, path = "windows.rs")]
mod os;
```

### Note

```rustc
#[cfg_attr(target_os = "linux", cfg_attr(feature = "multithreaded", some_other_attribute))
```
is equivalent to
```rustc
#[cfg_attr(all(target_os = "linux", feature ="multithreaded"), some_other_attribute)]
```
