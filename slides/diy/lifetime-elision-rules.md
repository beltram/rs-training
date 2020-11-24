## lifetime elision rules
* Writing lifetimes at any point in the code is called a *lifetime position*
    * `&'a T`
* Lifetime positions can be written for *input*, or *outputs*
* Lifetimes indicate how long a variable need to be alive, kind of like a scope
* They are to be specified for functions, pointer functions and closure traits 
* To increase readability, it is possible to avoid writing lifetime positions in certain cases:
    *  Each elided lifetime in input position becomes a distinct lifetime parameter.
    ```rust
    fn print(s: &str);                                      // elided
    fn print<'a>(s: &'a str);                               // expanded
    ```
    * If there is exactly one input lifetime position (elided or not), that lifetime is assigned to all elided output lifetimes.
    ```rust
    fn substr(s: &str, until: usize) -> &str;               // elided
    fn substr<'a>(s: &'a str, until: usize) -> &'a str;     // expanded
  
    fn new(buf: &mut [u8]) -> BufWriter;                    // elided
    fn new<'a>(buf: &'a mut [u8]) -> BufWriter<'a>          // expanded
    ```
    * If there are multiple input lifetime positions, but one of them is &self or &mut self, the lifetime of self is assigned to all elided output lifetimes.
    ```rust
    fn get_mut(&mut self) -> &mut T;                        // elided
    fn get_mut<'a>(&'a mut self) -> &'a mut T;              // expanded
    
    fn args<T: ToCStr>(&mut self, args: &[T]) -> &mut Command                  // elided
    fn args<'a, 'b, T: ToCStr>(&'a mut self, args: &'b [T]) -> &'a mut Command // expanded
    ```
    * Otherwise, it is an error to elide an output lifetime.
    ```rust
    fn get_str() -> &str;                                   // ILLEGAL, no inputs to infer from
    fn frob(s: &str, t: &str) -> &str;                      // ILLEGAL, cannot know whether to use first or second lifetime
  ```
