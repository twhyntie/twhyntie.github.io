---
title: Accessing an XNAT instance with Python
---
# Accessing an XNAT instance with Python
So it turns out you can access a remote XNAT instance using Python. You'll need to install the `pyxnat` module:

```bash
$ pip install pyxnat
```

This will let you play with the XNAT Interface wrapper:

```python
from pyxnat import Interface

## The XNAT interface object
xi = Interface()

# You'll be asked for the server, username, and password when the script is run.

# Disconnect.
xi.disconnect()
```

_You'll need to disconnect or your session will stay open. This could probably be handled more gracefully with some sort of `with`-type functionality..._

You can also supply the following arguments to the `Interface` constructor:

* `user`: your username on the XNAT instance;
* `password`: your password on the XNAT instance (careful!);
* `server`: the address of the XNAT server;
* `cachedir`: the location of the local cache directory, e.g. `/tmp`.
