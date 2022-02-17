# Python

## Environment variables
```
import os
USER = os.getenv('API_USER')
PASSWORD = os.environ.get('API_PASSWORD')
```

# 3rd Party Libraries
## Requests
https://requests.readthedocs.io/en/master/

### Post JSON data
```
import requests
url='https://api.github.com/some/endpoint'
payload={"data":"value"}
r = requests.post(url, json=payload)
```

## Pandas
Read JSON data
* [How to convert JSON into a Pandas DataFrame | Towards Data Science](https://towardsdatascience.com/how-to-convert-json-into-a-pandas-dataframe-100b2ae1e0d8)
```
import pandas as pd
df = pd.read_json('data.json')
print(df)
```

Calculate column
```
df['percent'] = df['rent']/df['total']
```

Print selected columns
```
selection = df[['Name', 'Age', 'Height']]
print(selection)
```

Merging dataframes
* [Joining DataFrames in Pandas | DataCamp](https://www.datacamp.com/community/tutorials/joining-dataframes-pandas)

# Command Line Stuff
## Virtual Environments
```
python3 -m venv /path/to/new/virtual/environment
```

## Web server
* Serve files from local directory
```python3 -m http.server 8000```
