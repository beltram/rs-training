## Nom
<img src="lib/images/nom.svg" style="height:40vh"/>   
[📒](https://docs.rs/nom/5.0.1/nom/) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3b90d7d21fc5be805765ce3c4461e677)

<!--
use nom::{
  IResult,
  sequence::delimited,
  character::complete::char,
  bytes::complete::is_not
};

/// Matches a sequence between parenthesis
fn parens(input: &str) -> IResult<&str, &str> {
  delimited(char('('), is_not(")"), char(')'))(input)
}
-->