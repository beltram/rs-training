## Performance
*Json Resp/s at x concurrent request (July 2019)*  

|Fmk|32|128|512|latency|
|:-------:|:-------:|:------:|:--------:|:--------:|
|actix-raw|424,934|999,238|1,356,789|0.3ms|
|vertx|403,088|891,996|1,328,626|0.4ms|
|spring|75,873|13,473|70,466|2.6ms|
|nodejs|303,349|548,899|550,371|0.5ms|
[link](https://www.techempower.com/benchmarks/#section=data-r18&hw=ph&test=json)