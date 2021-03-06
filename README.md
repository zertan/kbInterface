# kbInterface
This is a very early (alpha) version python+MATLAB interface to the new [KBase data API](https://github.com/kbase/data_api).

## Installation:

#### PyPi
```bash
pip install -e git+https://github.com/zertan/data_api#egg=doekbase_data_api-0.1.0 kbInterface
```

#### Git
```bash
git clone git@github.com:zertan/kbInterface.git
cd kbInterface
python setup.py install
```

#### Matlab (extra)
```matlab
addpath('[git clone path]/structFromPyObj.m')
```

## Usage:

#### Python
```python
import kbInterface
kb=kbInterface.get('[workspaceID]/[resourceID]')
kb.get_features()
```

#### Matlab
```matlab
kb=py.kbInterface.get('[workspaceID]/[resourceID]');
features=kb.get_features();
features=structFromPyObj(features) % convert to matlab struct
```

Please save valid KBase account info (json format) to '~/.kbacc' in your home directory (**or** just run kbInterface.get() in python). The resource **must** be in a KBase workspace that you have access to (IDs can be found in the KBase narrative). Tested on MacOS X El Capitan.

[![PyPI version](https://badge.fury.io/py/kbInterface.svg)](https://badge.fury.io/py/kbInterface)
