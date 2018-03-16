# yield-from

[![PyPI version](https://badge.fury.io/py/yield-from.svg)](https://badge.fury.io/py/yield-from)
[![Liberapay receiving](https://img.shields.io/liberapay/receives/hchasestevens.svg)](https://liberapay.com/hchasestevens/)

A backport of `yield from` from Python 3 to Python 2.7.

For more information, see https://github.com/hchasestevens/hchasestevens.github.io/blob/master/notebooks/backporting-yield-from-to-python-27.ipynb

## Installation
```bash
pip install yield-from
```

## Usage
```python
>>> from yieldfrom import yield_from, rewrite_yield_from
>>> def inner():
...   yield 'inner'
...
>>> @rewrite_yield_from
... def outer():
...   yield 'outer start'
...   yield_from(inner())
...   yield 'outer end'
...
>>> list(outer())
['outer start', 'inner', 'outer end']
```

## Contacts

* Name: [H. Chase Stevens](http://www.chasestevens.com)
* Twitter: [@hchasestevens](https://twitter.com/hchasestevens)
