# ApacheSpark

### Map vs Flatmap

```
sc.parallelize([3,4,5]).map(lambda x: [x,  x*x]).collect() 
Output:
[[3, 9], [4, 16], [5, 25]]

sc.parallelize([3,4,5]).flatMap(lambda x: [x, x*x]).collect()
Output: notice flattened list
[3, 9, 4, 16, 5, 25]
```
