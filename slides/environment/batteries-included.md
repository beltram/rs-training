## Batteries included
* Once compiled, requires no runtime locally
* Promotes external command avoidance ([openssl](https://crates.io/crates/openssl), 
  [git2](https://crates.io/crates/git2), 
  [k8s-openapi](https://crates.io/crates/k8s-openapi))
* Docker 😍

```
FROM rust:1.31
COPY ./ ./
RUN apt-get update 
RUN cargo build --target x86_64-unknown-linux-musl --release
RUN cp target/x86_64-unknown-linux-musl/release/app
FROM scratch
COPY --from=build target/x86_64-unknown-linux-musl/release/app
CMD ["/app"]
```