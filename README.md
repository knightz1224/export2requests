# Mitm export extra
This is a [mitmproxy addon](https://docs.mitmproxy.org/stable/addons-overview/) script, it exports request to python script, so you can re-request by using python-requests library.

Requirement
-----

Python 3.8 or above


Usage
-----

Use as addon for mitmproxy command:

```Bash
mitm_export_extra
```

Select a flow, and input the export command:

```vim
:export.requests @focus example_requests.py
```

Open the ```example_requests.py``` file:

```python
import requests

headers = {
        "accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8",
        "accept-encoding": "gzip, deflate, br",
        "accept-language": "en-US,en;q=0.5",
        "te": "trailers",
        "upgrade-insecure-requests": "1",
        "user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:87.0) Gecko/20100101 Firefox/87.0"
    }

response = requests.get("https://example.com/", headers = headers)

print(response.text)

```

License
-------

GPL 3.0
