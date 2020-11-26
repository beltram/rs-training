## lifetime elision rules
* Writing lifetimes at any point in the code is called a *lifetime position*
    * `&'a T`
* Lifetime positions can be written for *input*, or *outputs*
* Lifetimes indicate how long a variable need to be alive, kind of like a scope
* They are to be specified for functions, pointer functions and closure traits 
* To increase readability, it is possible to avoid writing lifetime positions in certain cases:

[📒](https://doc.rust-lang.org/reference/lifetime-elision.html)