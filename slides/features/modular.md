## Modularity the good way 

```rust
mod app {
    mod api {
        use super::client;
        pub fn on_request() {
            data::persist();
            // error ; data::mongo is 2 level below
            //data::mongo::persist();
            client::call();
        }
        fn list() {}
        mod data {
            // I can access private mod of my parents
            use super::super::client;
            pub fn persist() { client::call() }
            mod mongo { pub fn persist() {} }
        }
    }
    mod client { pub fn call() {} }
    fn call_api() {
        // error ; data is private in api
        //api::data::persist()
        api::on_request();
        // error ; I can't access private methods
        //api::list();
    }
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/crates-and-modules.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=6fb61734f410fc569cc4ccd0c5392690)