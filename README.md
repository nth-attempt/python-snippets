# python-snippets

<hr>

iter long list as chunks of fixed size
```python
from itertools import zip_longest

def grouper(iterable, chunk_size, fillvalue=None):
  return zip_longest(*[iter(iterable)]*chunk_size, fillvalue=fillvalue)
  
vals = range(45)
for chunk_vals in grouper(vals, chunk_size=10, fillvalue=None):
  print(chunk_vals)
```

<hr>

