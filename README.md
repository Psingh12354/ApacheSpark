# ApacheSpark

### Map vs Flatmap

**Map** :It returns a new RDD by applying a function to each element of the RDD.   Function in map can return only one item.

**FlatMap** : Similar to map, it returns a new RDD by applying  a function to each element of the RDD, but output is flattened.

```
sc.parallelize([3,4,5]).map(lambda x: [x,  x*x]).collect() 
Output:
[[3, 9], [4, 16], [5, 25]]

sc.parallelize([3,4,5]).flatMap(lambda x: [x, x*x]).collect()
Output: notice flattened list
[3, 9, 4, 16, 5, 25]
```
