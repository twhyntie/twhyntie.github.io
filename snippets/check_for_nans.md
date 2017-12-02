---
title: Checking for NaNs
---

# Checking for NaNs in a dataset

If you're importing data from a CSV or text file, there may be NaNs in there. If you don't check for them,
they can muck up further calculations or operations with funny error messages (bad) or without funny error messages
(even worse). So, it's worth checking for them once you've loaded your data.

If X is your `numpy` array that may or may not contain NaNs, you can count the NaNs with:

```python
import numpy as np
n_nans = np.count_nonzero(np.isnan(X))
```

If `n_nans` is non-zero, you'll need to investigate _why_ you're getting NaNs.
