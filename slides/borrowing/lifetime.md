## Lifetime
<img src="lib/images/lifetime.svg" style="height: 40vh"/>  
[📒](https://doc.rust-lang.org/1.7.0/book/lifetimes.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=075f8d7e47ab6e93732d4bf81ab81c46)

<!--
#[test]
fn salute() {
    let firstname: &str = "beltram";
    let lastname: &str = "maldant";
    assert_eq!("m", say_hi_and_get_initial(firstname, lastname));
}
fn say_hi_and_get_initial<'a>(firstname: &str, lastname: &'a str) -> &'a str {
    println!("👋 {}", firstname);
    &lastname[..1]
}
-->