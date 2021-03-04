# export2requests
This is a [mitmproxy addon] script, it exports request to python script, so you can re-request by using python-requests library.
[mitmproxy addon]: https://docs.mitmproxy.org/stable/addons-overview/

Usage
-----

Use as addon for mitmproxy command:

```
mitmproxy -s export2requests.py
```

Select a flow, and input the export command:

```
:export.requests @focus requests.py
```

License
-------

GPL 3.0
