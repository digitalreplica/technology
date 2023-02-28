is:: [[software]]
from:: [[linux]]

# Notes
jq is a cli tool to query json data

# Howto
## explore json file
```
jq '. | keys' file.json
```

## Iterate over a list or object
```
.[]
```

## Print list (without quotes or commas)
```
jq -r '.paths | keys | .[] '
```

## Printing two fields
jq '.[] | .field1 + " " + .field2'

## Printing number
jq '.[] | (.field1|tostring)'

## Filters
```
jq ‘.results[] | select(.name == “John”) | {age}’      # Get age for ‘John’
jq ‘.results[] | select(.name | contains(“Jo”))’       # Get complete records for all names with ‘Jo’
jq ‘.results[] | select(.name | test(“Joe\s+Smith”))’  # Get complete records for all names matching PCRE regex ‘Joe\+Smith’
```

# Links

[jq Manual](https://stedolan.github.io/jq/manual/)
[jq Cheat Sheet](https://lzone.de/cheat-sheet/jq)
