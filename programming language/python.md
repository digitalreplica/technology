---
is: "[[programming language]]"
---
# Notes
- Python programming languages
## Strings
multiline strings - using triple quotes
```
"""line one
line two
"""
```
## Files
Read file
## Walrus operator :=
The `:=` (walrus) operator lets you assign and use a variable in the same line

# Standard libraries
## os
Environment variables
```
import os
USER = os.getenv('API_USER')
PASSWORD = os.environ.get('API_PASSWORD')
```
### os.path
- Path manipulation

File exists
```
import os
os.path.exists('filename')
```
## uuid
Create uuid
```
import uuid
my_uuid = str(uuid.uuid4())
```
# 3rd Party Libraries
## Requests
https://requests.readthedocs.io/en/master/

Post JSON data
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

Updating columns that meet a certain condition
```
df.loc[df['Quantity'] == 0, 'Quantity'] = df['Current Value']
```

Merging dataframes
* [Joining DataFrames in Pandas | DataCamp](https://www.datacamp.com/community/tutorials/joining-dataframes-pandas)

Dictionary or list of dicts to dataframe
```
mydata = [{'name': 'alice'}, {'name': 'bob'}]
df = pd.DataFrame.from_dict(mydata)
```

Removing `$` from numbers
```
df['Sales'] = df['Sales'].str.replace('$', '')
```

Renaming columns
```
df.rename(columns={"A": "a", "B": "c"})
```

Convert column to numbers
```python
df["a"] = pd.to_numeric(df["a"])
```

Sum a column
```
df['points'].sum()
```

Showing column types
```
print(df.dtypes)
```

Saving CSV
```
df.to_csv('file1.csv', index=False)
```
## Streamlit
- UI apps in python
- https://docs.streamlit.io/

# Command Line Stuff
## Virtual Environments
```
python3 -m venv /path/to/new/virtual/environment
```
or most commonly
```
python3 -m venv venv3
source venv3/bin/activate
python --version
```

## Web server
* Serve files from local directory
```python3 -m http.server 8000```

## Pip
### Updating
```
pip install --upgrade pip
```

### Updating packages
