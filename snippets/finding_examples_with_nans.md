---
title: Finding examples with NaNs in a DataFrame
---

# Finding examples containing NaNs in a DataFrame

Got a DataFrame that may contain NaNs in one or more of its rows?  Select them
with the following code:

```python
df_nans = df[df.isnull().any(axis=1)]
```

_Note that, sticking to the terminology of Machine Learning, we're referring to 
rows of a `DataFrame` as **examples** (the whole `DataFrame` itself being the
**Design Matrix**._
