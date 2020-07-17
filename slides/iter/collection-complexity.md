## Data structure

* 'n' is size of collection, 'm' is the size of another collection if involved

||get(i)|insert(i)|remove(i)|append|
|:-------:|:-------:|:------:|:--------:|:--------:|
|**Vec**|O(1)|O(n-i)|O(n-i)|O(m)|
|**VecDeque**|O(1)|O(min(i, n-i))|O(min(i, n-i))|O(m)|
|**LinkedList**|O(min(i, n-i))|O(min(i, n-i))|O(min(i, n-i))|O(1)|
|**Hash(Map/Set)**|O(1)|O(1)|O(1)|N/A|
|**BTree(Map/Set)**|O(log(n))|O(log(n))|O(log(n))|O(n+m)|

[📒](https://doc.rust-lang.org/std/collections/index.html#sequences)