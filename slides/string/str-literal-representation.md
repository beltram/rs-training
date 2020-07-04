## string literal

```bash
                               pointer
                             /   length
                           /   / 
                         /   / 
                      +–––+–––+
           stack      │ • │ 6 │ <- a_string_literal: &str
                      +–│–+–––+
                        │
                        +––––––––––+
                                   │
           preallocated  +–––+–––+–V–+–––+–––+–––+–––+–––+–––+–––+
           read-only     │ ? │ ? │ P │ a │ s │ c │ a │ l │ ? │ ? │
           memory        +–––+–––+–––+–––+–––+–––+–––+–––+–––+–––+
```