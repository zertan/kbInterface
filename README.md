# kbInterface
This is a very early (alpha) version MATLAB interface to the new [KBase data API](https://github.com/kbase/data_api).

## Usage:

#### Python
```python
import kbInterface
kb=kbInterface.get('[workspaceID]/[resourceID]')
kb.get_features()
```

#### Matlab
```matlab
kb=py.kbInterface.get(['14606/' genomes{2}])
kb.get_features()
```

Please save valid KBase account info to '~/.kbacc' in your home directory. Tested on MacOS X El Capitan.

[![PyPI version](https://badge.fury.io/py/kbInterface.svg)](https://badge.fury.io/py/kbInterface)
