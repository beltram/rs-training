## Fearless concurrency 
<img src="lib/images/thread-safe.svg" style="height: 40vh"/>  
[📒](https://doc.rust-lang.org/1.7.0/book/concurrency.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=46cba10e3dde1ca0e8f8d54d653eaa16)

<!--
use std::{sync::{Arc, Mutex}, thread};
use rayon::prelude::*;
fn send_chunks() {
    let movie = "👽☝️🚴";
    let movie_rc = Arc::new(movie).clone();
    thread::spawn(move || { println!("Send {}", movie_rc) });
    thread::spawn(move || { println!("Send {}", movie) });
    let mut comic = Arc::new(Mutex::new("🌕👦"));
    let comic_mutex = comic.clone();
    thread::spawn(move || {
        comic_mutex.lock()
            .map(|ref mut com| com.replace("👦", "🐵"))
            .map_err(|e| "Failed acquiring 🔒");
    });
    vec!["🚀👨", "👩☁️💎"].par_iter()
        .for_each(|song| println!("Listen {}", song));
}
-->