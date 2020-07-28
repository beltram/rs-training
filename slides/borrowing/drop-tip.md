## Drop advanced tip

* ONLY IF you have to drop large objects and do not want to slow down the main thread
* you can move the object to a background thread which will drop it in //

```rust
struct Picture { name: &'static str, painted_by: &'static str, blob: String }
impl Drop for Picture {
    fn drop(&mut self) { println!("Dropping picture {}", self.name); }
}
fn about_picture(pic: Picture) -> String {
    let about = format!("The {} was painted by {}", pic.name, pic.painted_by);
    std::thread::spawn(move || pic);
    // thread takes ownership of pic.blob and will deallocate it once it ends
    about
}
fn main() {
    let blob: String = std::str::from_utf8(&[1; 10_000]).unwrap().to_string();
    let joconde = Picture { name: "Joconde", painted_by: "Leonardo", blob };
    println!("{}", about_picture(joconde));
}
```