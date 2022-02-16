# Python

# Virtual Environments
```
python3 -m venv /path/to/new/virtual/environment
```

# Requests
https://requests.readthedocs.io/en/master/

## Post JSON data
```
import requests
url='https://api.github.com/some/endpoint'
payload={"data":"value"}
r = requests.post(url, json=payload)
```

## Environment variables
```
import os
USER = os.getenv('API_USER')
PASSWORD = os.environ.get('API_PASSWORD')
```

# Web server
* Serve files from local directory
python3 -m http.server 8000
