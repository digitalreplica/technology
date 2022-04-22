# Atom

[Atom](https://atom.io/) is Github's text editor.

# Tips
## Copying relative file paths
From the root directory:
* Select a file in the tree view, right-click and select "Copy Project Path".

From the current file being edited:
* Install the tree-view-copy-relative-path plugin
* Select a file in the tree view, right-click and select "Copy Relative Path".

## Open a new window using the current directory
```
atom -n .
```

Or on MacOS
```
open -a atom.app -n .
```

## Invisible Text
Change styles
```
atom-text-editor {
  color: hsl(180, 24%, 12%);
}
```

## Showing markdown preview
```ctrl-shift-m```

## Creating Finder Quick Action on Mac
* Open Automator
* New -> Quick Action
* Workflow receives "folders" in "Finder.app"
* Run Shell script, /bin/bash, input as arguments
* /Applications/Atom.app/Contents/MacOS/Atom -n "$@"

## Paste link as markdown
* Add a command to [paste links as markdown](https://flight-manual.atom.io/hacking-atom/sections/the-init-file/)

# Adding Finder "Open in Atom" Quick Action menu
* https://gist.github.com/idleberg/874790e8e3c8b1419e4439d0a48d2aa5
