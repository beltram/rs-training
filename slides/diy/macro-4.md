## Procedural macro
* function-like macros
    * uses `!` macro operator
    * apply treatment on parameters 
    * allows variable parameter number
    
  ```rust
    let sql = sql!(SELECT * FROM posts WHERE id=1);
  ```
  ```rust
    #[proc_macro]
    pub fn sql(input: TokenStream) -> TokenStream {
      // implementation    
    }
  ```