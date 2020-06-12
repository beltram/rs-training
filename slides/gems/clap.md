## Clap
<img src="lib/images/clap.svg" style="height:40vh"/>    
[📒](https://docs.rs/clap/2.33.0/clap) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=13c7bc439f9060e5c83ab80bbe43d3f5)   

<!--
let blame_beltram = vec!["guilt", "blame", "-w", "beltram"];
        let help = vec!["guilt", "--help"];
        let app = App::new("Guilt")
            .version("1.0")
            .author("John Doe<jdoe@gmail.com>")
            .about("Blames someone")
            .subcommand(SubCommand::with_name("blame")
                .about("Output a blame history")
                .version("1.3")
                .author("Maria Doe<mdoe@outlook.com>")
                .arg(Arg::with_name("who")
                    .short("w")
                    .value_name("WHO")
                    .takes_value(true)
                    .help("Who to blame")));
        if let Some(matches) = app.clone().get_matches_from(blame_beltram).subcommand_matches("blame") {
            println!("Ooops {} I did it again", matches.value_of("who").unwrap());
        }
        println!("--------------------");
        println!("Generated help: ");
        println!("{:?}", app.clone().get_matches_from(help));-->
