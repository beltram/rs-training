## Vec of String in memory

```rust
let vec: Vec<String> = vec![String::from("alpha"), String::from("beta")];
```

```bash
+-----+-----+-----+
|  •  |  2  |  2  |
+--│--+-----+-----+
   │
[–-│–– alpha –––––][–--–– beta –––––]
+--V--+-----+-----+-----+-----+-----+
|  •  |  5  |  5  |  •  |  4  |  4  |
+--│--+-----+-----+--│--+-----+-----+
   │                  ‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾│
+--V--+-----+-----+-----+-----+     +--V--+-----+-----+-----+
|  a  |  l  |  p  |  h  |  a  |     |  b  |  e  |  t  |  a  |
+-----+-----+-----+-----+-----+     +-----+-----+-----+-----+
```