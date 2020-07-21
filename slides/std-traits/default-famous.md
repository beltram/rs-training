## [Default](https://doc.rust-lang.org/std/default/trait.Default.html) of standard types

|  Type | Default ||  Type | Default |
|:-------:|:------:|:-------:|:-------:|:------:|
|`Option<T>`|None|│|f32, f64|0.0|
|`Result<T, E>`|Ok(T::default())|│|char|'\x00'|
|String|String::new()|│|`&[T]`|&[]|
|bool|false|│|`[T; N]`|[T::default(); N]|
|u8,..i32|0|│|`Vec<T>`|Vec::new()|




