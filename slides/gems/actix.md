## Actix
<img src="lib/images/actix.svg" style="height:40vh"/>  
[📒](https://actix.rs/) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=e9f0f4bbb63e3a2da69daa14051322e9)

<!--
use actix_web::{middleware, web, App, HttpRequest, HttpServer};

fn index(req: HttpRequest) -> &'static str {
    println!("REQ: {:?}", req);
    "Hello world!"
}

fn main() -> std::io::Result<()> {
    std::env::set_var("RUST_LOG", "actix_web=info");
    env_logger::init();

    HttpServer::new(|| {
        App::new()
            // enable logger
            .wrap(middleware::Logger::default())
            .service(web::resource("/index.html").to(|| "Hello world!"))
            .service(web::resource("/").to(index))
    })
    .bind("127.0.0.1:8080")?
    .run()
}
-->