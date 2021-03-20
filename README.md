# python-snippets


iter long list as chunks of fixed size
```python
from itertools import zip_longest

def grouper(iterable, chunk_size, fill_value=None):
  return zip_longest(*[iter(iterable)]*chunk_size, fill_value=fill_value)
  
vals = range(45)
for chunk_vals in grouper(vals, chunk_size=10, fill_value=None):
  print(chunk_vals)
```
