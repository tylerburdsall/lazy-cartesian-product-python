# lazy-cartesian-product
Find the Nth entry in a Cartesian Product

## Usage
Given a list of lists, you can find the Nth entry in a Cartesian Product without precomputing every combination. This saves memory and time while also maitaning close to O(1) performance:

```
from LazyCartesianProduct import LazyCartesianProduct

def example():
  a = [ 1, 2, 3, 4, 5 ]
  b = [ 'foo', 'bar' ]
  c = [ 'x', 'y', 'z' ]
  d = [ 'one', 'two', 'three' ]

  sets = [ a, b, c, d ]

  cp = LazyCartesianProduct(sets)

  result1 = cp.entryAt(8)
  print(result1)

  result2 = cp.entryAt(32)
  print(result2)

  result3 = cp.entryAt(67)
  print(result3)
  
 example()
```

When ran, the following output is produced:

```
$ python example.py
[1, 'foo', 'z', 'three']
[2, 'bar', 'y', 'three']
[4, 'bar', 'y', 'two']
$
```

## License
BSD-2, see LICENSE
