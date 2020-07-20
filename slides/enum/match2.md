## match control flow with enum

* match expression can be used to access variant data directly (often used with Option and Result enum)

```Rust
fn get_workplace_insight(workplace: WorkplaceDetailed) -> () { 
    match workplace {
        WorkplaceDetailed::Paris(office) => println!("Office's name is Paris, {}", office),
        WorkplaceDetailed::Nantes(office) => println!("Office's name is Nantes, {}", office),
    }
}

fn main() {
    // will print: Office's name is Paris, Kleber
    get_workplace_insight(WorkplaceDetailed::Paris("Kleber".to_string()));
}
```

[📒](https://doc.rust-lang.org/book/ch06-02-match.html)