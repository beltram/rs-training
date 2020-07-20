## if let control flow with enum

* You can handle values that match one pattern in a less verbose way with if let (without exhaustivity check though)
* It's some kind of sugar syntax when you don't need to handle all the cases
```Rust
let workplace = WorkplaceDetailed::Paris(String::from("Kleber"));
if let WorkplaceDetailed::Paris("Kleber".to_string()) = workplace {
	println!("This is the boss's office");
}
```

* This is striclty equivalent to
```Rust
let workplace = WorkplaceDetailed::Paris(String::from("Kleber"));
match workplace {
	WorkplaceDetailed::Paris("Kleber".to_string()) => println!("This is the boss's office"),
	_ => (),
}
```

[📒](https://doc.rust-lang.org/book/ch06-03-if-let.html)