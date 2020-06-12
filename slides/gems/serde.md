## Serde
<img src="lib/images/serde.svg" style="height:40vh"/>  
[📒](https://serde.rs/) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3633cb4437d21831d680af853b3cfd3e)

<!--
use serde::*;
#[derive(new, Clone, Debug, Default, Serialize, Deserialize)]
#[serde(default)]
struct Dog { name: String, color: String }

#[test]
fn test() {
    let dog = Dog::new("Rex".to_string(), "black".to_string());
    let to_yaml = serde_yaml::to_string(&dog).unwrap();
    let to_json = serde_json::to_string(&dog).unwrap();
    println!("To yaml {:#?}", to_yaml);
    println!("To json {:#?}", to_json);
    let from_yaml: Dog = serde_yaml::from_str(&to_yaml).unwrap();
    let from_json: Dog = serde_json::from_str(&to_json).unwrap();
    println!("From yaml: {:#?}", from_yaml);
    println!("From json: {:#?}", from_json);
}
-->