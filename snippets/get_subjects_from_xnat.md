---
title: How can I get a list of subjects from the XNAT instance?
---

# Getting a list of subjects from the XNAT instance

This'll get you a list of the subjects (i.e. patients) in the projects of your XNAT instance:

```python
from pyxnat import Interface

## The XNAT interface - supply arguments or enter them interactively.
xi = Interface()

## A list of the subjects in all projects.
subjects = xi.select.projects().subjects().get()

# Update the user.
print(subjects)
```
