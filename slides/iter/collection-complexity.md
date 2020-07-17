## Data structure

||get(i)|insert(i)|remove(i)|append|
|:-------:|:-------:|:------:|:--------:|:--------:|
|**Vec**|O(1)|O(n-i)|O(n-i)|O(m)|
|**VecDeque**|O(1)|O(min(i, n-i))|O(min(i, n-i))|O(m)|
|**LinkedList**|O(min(i, n-i))|O(min(i, n-i))|O(min(i, n-i))|O(1)|
|**HashMap**|O(1)|O(1)|O(1)|N/A|
|**BTreeMap**|O(log(n))|O(log(n))|O(log(n))|O(n+m)|

*Set complexity == Map complexity*