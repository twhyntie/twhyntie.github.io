---
title: How can I get MR session data from an XNAT instance?
---

# Getting the MR session data from an XNAT instance

```python
from pyxnat import Interface

## The XNAT interface object.
xi = Interface()

## A JSON-like object containing all of the MR session data.
session_data = xi.select('xnat:mrSessionData').all()

# Take a cheeky peek (careful if you've got a lot in there...!).
for exp in session_data:
    print(exp)
    break
```
