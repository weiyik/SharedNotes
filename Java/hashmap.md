# HashmMap

## HashMap-JDK7

* Array + LinkedList
* Index of array: `hash(key.hashcode()) & length - 1`, where `length` of buckets array must be power of 2
* Above indexing method only use the lower bits, to further distribute the indexes, `hash` method use XOR operation to bring higher bits into consideration.
