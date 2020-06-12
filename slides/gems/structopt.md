## Structopt
<img src="lib/images/structopt.svg" style="height:40vh"/>  
[📒](https://docs.rs/structopt/0.3.3/structopt/) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=684eee38a092b67a255bbe2f2d8ebdbd)

<!--
#[derive(StructOpt, Debug)]
#[structopt(name = "guilt")]
struct Guilt {
    // This is the -h message
    //
    // and this is the --help message
    #[structopt(short = "d", long = "debug")]
    debug: bool,
    #[structopt(subcommand)]
    cmd: Commands,
}
        
#[derive(Debug, StructOpt)]
#[structopt(rename_all = "kebab-case")]
pub enum Commands {
    Blame {
        who: String,
    },
}
        
println!("{:?}", Guilt::from_args());
-->