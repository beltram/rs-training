## String
<img src="lib/images/string.svg" style="height: 40vh"/>  
[📒](https://doc.rust-lang.org/1.7.0/book/strings.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=759eebce54df6844d10fc147b7f76df1)

<!--
let empty_string: String = String::new();
let also_empty_string: String = String::default();
let string_litteral: &str = "I am allocated on the stack";
let from: String = String::from("I am allocated on the heap");
let like_from: String = "I am the same as from".to_string();
let utf8: &str = "I am also utf-8 encoded";
let utf8: &str = "أنا أيضا utf-8 المشفرة";
let mut growable: String = String::from("kameha");
growable.push_str("meha");
let i_will_be_moved: String = String::from("E=");
let formula: String = i_will_be_moved + "MC2";
let formula: String = format!("{}={}", "E", "MC2");
let hello: &str = &"hello world!"[..5];
let nihao: &str = &"你好"[..1];
-->
