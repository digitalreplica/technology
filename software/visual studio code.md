---
is_a:
  - "[[software]]"
urls:
  - https://code.visualstudio.com/
---
# About
- programming IDE

Setup CLI command on mac
- https://code.visualstudio.com/docs/setup/mac

Search and replace with regex
- replace `"quantity": "([\d\.]+)",` with `"quantity": $1,`

Open a folder in MacOS Finder
- Create an Automator Quick action
	- `Open Finder Items`, and open with `Visual Studio Code`

Edit a line in all files
- select `edit`, `replace in files`. Review the preview then click the `Replace all` button
- https://code.visualstudio.com/docs/editor/codebasics#_search-and-replace

Replace `\n` with newline
- Search for `\n`, replace with <crtl><enter>

Setting environment variables
- https://code.visualstudio.com/docs/python/environments#_environment-variables
- make a file ending in `.env`, like `sandbox.env`
```
MY_VAR=foo
```
