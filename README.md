PyBittrex
=========

Compatibility
-------------
Compatible with Python 2 and 3.

Prerequisites
-------------
1. Register for a Bittrex account
2. Enable Two Factor authentication
3. Generate an API Key and Secret

Installation
------------
```
pip install pybittrex
```

Usage
-----
Everything is handled through a client object.  Instantiate it using your API key and API secret:

```python
from pybittrex.client import Client

c = Client(api_key='abc', api_secret='123')
```

The library returns a [Requests](https://docs.python-requests.org/en/master) object, so you can access all the parts of the returned data as you would if you were working with it natively:

```python
markets = c.get_markets().json()['result']

for i in markets:
    print(i['MarketName'])
```

License
-------
PyBittrex is licensed under the MIT license.
