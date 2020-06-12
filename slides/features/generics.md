## Generics
<img src="lib/images/generics.svg" style="height:40vh"/>  
[📒](https://doc.rust-lang.org/1.7.0/book/generics.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=d2f16e78a80b4547d1551e5e3cce834e)

<!--
use std::fmt::{Display, Formatter, Error};
    
trait Eatable {}
struct Lemon {}
impl Eatable for Lemon {}
impl Display for Lemon {
    fn fmt(&self, f: &mut Formatter) -> Result<(), Error> { 
    	write!(f, "🍋") 
  	}
}
    
trait Human<T> where T: Eatable + Display {
    fn eat(food: T) { println!("Miam {}", food) }
}
    
struct Cyril {}
impl Human<Lemon> for Cyril {}
-->
