## Borrowing 
###### Introducing move
<img src="lib/images/move.svg" style="height: 13vh"/>
```console
let s1: String = String::from("hello");
    -- move occurs because `s1` has type `std::string::String`, 
    which does not implement the `Copy` trait
let s2: String = s1;
                 -- value moved here
println!("{:?} world", s1);
                       ^^ value borrowed here after move
```  
[📒](https://doc.rust-lang.org/1.7.0/book/ownership.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3f5767b8b83635d49723d1be198c8eb6)

<!--
fn do_stuff() {
    let s1: String = String::from("hello");
    let s2: String = s1;
    println!("{:?} world", s1);
}
-->