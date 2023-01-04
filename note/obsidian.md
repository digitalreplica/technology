---
tags: a/note
---
in:: [[technology]]

# Notes
Markdown notes app. Using it as a UI on top of git-based note repos

# Notes
## Links
* [Website](https://obsidian.md/)
* [Help](https://help.obsidian.md/Obsidian/Index)
	* [Format your notes](https://help.obsidian.md/How+to/Format+your+notes)
	* [Embedded queries](https://help.obsidian.md/Plugins/Search#Embed+search+results)
* [Forums](https://forum.obsidian.md/)
* [ObsidianMD | Reddit](https://www.reddit.com/r/ObsidianMD/)

### Other Resources
- [Obsidian Roundup](https://www.obsidianroundup.org/resources/) has links to many Obsidian-related resources

## Plugins
- [[obsidian dataview]]
- [juggl](https://juggl.io/Juggl)

### Breadcrumbs
- [breadcrumbs documentation](https://breadcrumbs-wiki.onrender.com/docs/Home)
- [breadcrumbs discussions](https://github.com/SkepticMystic/breadcrumbs/discussions)
- a note can have multiple parents

Codeblock for down nodes (Remove `#` at end of breadcrumns)
```breadcrumbs#
type: tree
dir: down
depth: -1
from: -"_templates"
```

Codeblock for tags
```
BC-tag-note: #Tag
BC-tag-note-field: down
```
## Home page ideas
- https://forum.obsidian.md/t/the-all-encompassing-obsidian-homepage-template-at-least-i-hope-so/30378

## Preferences
Function | Hotkey | Notes
--- | --- | ---
Insert Template | apple-T
Insert current date | apple-shift-8 | Mimic Bear notes

## Ideas
- Find or make module to open links in private browser window
- Try [tracking books in obsidian](https://beingpax.medium.com/how-to-create-a-bookshelf-to-track-books-in-obsidian-f5130555be44)
- Try dataview plugin. https://blacksmithgu.github.io/obsidian-dataview/
- Look for git plugins

# HowTo
## Quick things
- Quickly switch between two notes
	- Hotkeys: `Command`->`Option`->`Left arrow`
	- Using Open command: `Ctrl/Cmd+O` → `Down arrow` → `Enter`.
	- [Callouts](https://help.obsidian.md/How+to/Use+callouts): `> [!INFO]`

## Snippets
**Aliases**
- Set in front matter at the top of a note
```
---
aliases: [AI, Artificial Intelligence]
---
```

**Lists in front matter**
```
key3: [one, two, three]
key4:
- four
- five
- six
```

**Creating a Github repo list using the github cli**
```
# Repos
Repo | Private | Description
---- | ---- | ----
```
```
gh repo list --json name,owner,url,isPrivate,description --template '{{range .}}{{printf "[%s](%s) | %t | %s\n" .name .url .isPrivate .description}}{{end}}' | sort
```

**Convert Untappd export to obsidian objects**
```
jq -r '.[] | "- [x] #do/drink/beer [name:: " + .beer_name + "],[style:: " + .beer_type + "],[brewery:: " + .brewery_name + "],[abv:: " + .beer_abv + "],[rating:: " + .rating_score + "],[✅" + .created_at + "]"' 068c524db602738a5eb00eb4747a7ed9.json >beer-list.md
```

# Css
- https://help.obsidian.md/How+to/Add+custom+styles
	- add override in `YOUR_VAULT/.obsidian/snippets/YOUR_CUSTOM_SNIPPET.css`

# Potentially interesting plugins 
- https://github.com/holubj/obsidian-dialogue-plugin - Create dialog in markdown
- https://github.com/deathau/sliding-panes-obsidian - Andy Matuschak Mode
- https://github.com/jdbrice/obsidian-code-block-copy - copy button for code blocks
- https://github.com/MamoruDS/obsidian-open-link-with - open links with specific browser, including private windows
- https://github.com/Darakah/obsidian-commits - track commits (like git, but not using git)
- https://github.com/Vinzent03/obsidian-hotkeys-for-specific-files
- https://github.com/Vinzent03/obsidian-shortcuts-for-starred-files
- https://github.com/zolrath/obsidian-auto-link-title - fetch titles for urls

# Questions
- Any way to query starred notes?
	- Feature request at https://forum.obsidian.md/t/make-starred-notes-searchable/15125
- Energy consumption?
- Try breadcrumbs plugin?