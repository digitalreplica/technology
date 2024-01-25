---
is: "[[howto]]"
of: "[[cli]]"
of: "[[digitalreplica/technology/software/bash]]"
---
# Notes

## Edit all files in a folder
- works on mac
```sh
for i in *
do
sed -i '' 's/style::/type::/g' $i
done
```

## Truncate part of a string match
- replacing a day wikilink with a month one. Ex: `[[2023-03-12]]` to `[[2023-03]]`
```sh
for i in *
do
sed -i '' -E 's/(\[\[[0-9][0-9][0-9][0-9]-[0-9][0-9])-[0-9][0-9]\]\]/\1\]\]/g' $i
done
```
