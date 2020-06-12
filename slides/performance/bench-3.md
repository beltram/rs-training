## Performance
*Plaintext Resp/s at x concurrent request (July 2019)*  

|Fmk|256|1024|16,384|latency|
|:-------:|:-------:|:------:|:--------:|:--------:|
|actix|6,978,473|7,000,911|6,676,956|2.9ms|
|vertx|4,446,280|4,573,842|4,092,465|7.4ms|
|spring|25,080|27,893|70,573|158.6ms|
|nodejs|833,031|936,322|965,807|42.2ms|
[link](https://www.techempower.com/benchmarks/#section=data-r18&hw=ph&test=plaintext)