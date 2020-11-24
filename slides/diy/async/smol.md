## Smol
```rust
use std::net::{TcpListener, TcpStream};

use smol::{io, Async};

/// Echoes messages from the client back to it.
async fn echo(stream: Async<TcpStream>) -> io::Result<()> {
    io::copy(&stream, &mut &stream).await?;
    Ok(())
}

fn main() -> io::Result<()> {
    smol::block_on(async {
        // Create a listener.
        let listener = Async::<TcpListener>::bind(([127, 0, 0, 1], 7000))?;
        println!("Listening on {}", listener.get_ref().local_addr()?);

        loop {
            let (stream, peer_addr) = listener.accept().await?;
            // Spawn a task that echoes messages from the client back to it.
            smol::spawn(echo(stream)).detach();
        }
    })
}
```