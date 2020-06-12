## Performance
*Resp/s at x queries/request (July 2019)*  
*actix-1.0.0 / vertx-3.7.0 / spring-2.2.0.M2 / nodejs-12.3.1* 

|Fmk|1|10|20|latency|
|:-------:|:-------:|:------:|:--------:|:--------:|
|actix-core|891,980|93,318|46,968|10.8ms|
|vertx-postgres|718,446|90,294|44,979|11.3ms|
|spring-webflux-pgclient|152,005|69,707|31,522|16.2ms|
|nodejs|129,941|17,789|9,245|54.5ms|
[link](https://www.techempower.com/benchmarks/#section=data-r18&hw=ph&test=query)