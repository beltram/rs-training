## Borrowing 
###### Use reference or return
<img src="lib/images/ref-or-return.svg" style="height: 35vh"/>  
[📒](https://doc.rust-lang.org/1.7.0/book/references-and-borrowing.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=ea35bb5d7a990008c6badcb8a9cf719b)

<!--
fn do_stuff() {
    let s1: String = String::from("hello");
    salute(&s1);
    let s1 = to_deaf_lang(s1);
    to_deaf_lang(s1);
}

fn salute(hi: &String) { println!("{:?} world", hi) }

fn to_deaf_lang(to: String) -> String {
    println!("{} -> 👋", to);
    to
}
-->