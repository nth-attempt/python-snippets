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

iter from start_date to end_date of datetime objects
```python
import datetime

def daterange(start_date, end_date):
    for n in range(int((end_date-start_date).days)):
        yield start_date + datetime.timedelta(n), start_date + datetime.timedelta(n+1)

start_date = datetime.date(2020, 1, 1)
end_date = datetime.date(2020, 1, 31)
for start, end in daterange(start_date, end_date):
    print(start, end)
```

<hr>

TODO: add multiprocessing using pathos


TODO: add multiprocessing using Manager

TODO: pd set options for max rows, columns, column width

<hr>

visualize dataframe as a heatmap
```python
import numpy as np
import pandas as pd

index = [1, 2, 3, 4]
cols = ["A", "B", "C"]
df = pd.DataFrame(np.random.randn(4, 3), index=index, columns=cols)
df.style.background_gradient(cmap="Blues")
```

<hr>

