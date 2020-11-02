## .as_ref() / .as_mut()

* '.as_ref()'
  * `Option<T> --> Option<T>`
  * `Result<T, E> --> Result<&T, &E>`
  * also works for borrowed variants e.g. `&Option<T>`
* '.as_mut()'
  * `Option<T> --> Option<&mut T>`
  * `Result<T, E> --> Result<&mut T, &mut E>`
  * also works for borrowed variants e.g. `&mut Option<T>`