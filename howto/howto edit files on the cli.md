is:: [[howto]]
of:: [[cli]]

# Notes

## Edit all files in a folder
- works on mac
```
for i in *
do
sed -i '' 's/style::/type::/g' $i
done
```