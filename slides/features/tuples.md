## Native tuples
<img src="lib/images/tuples.svg" style="height:40vh"/>    
[📒](https://doc.rust-lang.org/rust-by-example/primitives/tuples.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=4df01a602dc40592591f884c5eb0bdce)

<!--
#[derive(new)]
struct Date {
    pub year: u16,
    pub month: u8,
    pub day: u8,
}
// aka zero cost abstraction    
struct TupleDate(u16, u8, u8);
    
fn calendar() {
    let second_poteau_pavaaard = Date::new(2018, 6, 30);
    let Date { year, month, day } = second_poteau_pavaaard;
    let (rep_year, rep_month, rep_day) = to_rep_date(second_poteau_pavaaard);
    let republican_calendar_start = TupleDate(1792, 9, 22);
    let ppcms = vec![(3, 5), (5, 11)].iter()
        .map(|(a, b)| a * b)
        .collect::<Vec<i32>>();
}
    
fn to_rep_date(date: Date) -> (u16, u8, u8) {
    (date.year - 1792, (12 + date.month - 9) % 12, date.day)
}
-->