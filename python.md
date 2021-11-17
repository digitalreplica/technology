# Python

# Requests
https://requests.readthedocs.io/en/master/

## Post JSON data
```
import requests
url='https://api.github.com/some/endpoint'
payload={"data":"value"}
r = requests.post(url, json=payload)
```

# Web server
* Serve files from local directory
python3 -m http.server 8000
