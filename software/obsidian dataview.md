---
is_a:
  - "[[software]]"
---

# Notes
File query language plugin for [[obsidian]].

# Help
- [obsidian-dataview | GitHub](https://blacksmithgu.github.io/obsidian-dataview/)
- [documentation](https://blacksmithgu.github.io/obsidian-dataview/)
- [Forum examples](https://forum.obsidian.md/t/dataview-task-and-project-examples/17011)

# Notes
YAML objects aren't really objects. With some frontmatter like
```
---
object:
	name: foo
is_a: "[[software]]"
of: "[[obsidian]]"
---
```

You can't query for `object.name`, only `name`. This will pull `name` from `object` , but also a plain name field, or one in a different object

## Interesting reads
- https://www.calliopesounds.com/2022/05/yet-another-obsidian-dataview-and-gtd.html

# HowTo
## Dataview query language
**Query notes for a given topic**
```
LIST WHERE contains(topic, this.file.name)
```

**Query community (community name is current file name)**
```
LIST FROM #person
WHERE contains(community, this.file.name)
```

**Query events from year note**
```
LIST FROM #event AND "event"
WHERE contains(file.name, this.file.name)
SORT file.name
```

**Query notes in the same folder or below**
```
LIST WHERE contains(file.folder, this.file.folder) SORT file.name
```

**Recent Files**
```
WHERE file.mtime >= date(now) - dur(7 days)
SORT file.mtime DESC
```

**Query topics**
```
TABLE WITHOUT ID link(file.link, file.folder) as Location
FROM #topic
WHERE !startswith(file.path, "templates")
SORT file.folder
```

**Sort date descending**: `sort file.mday desc`

**Create custom obsidian link**
```
TABLE WITHOUT ID link(file.link, file.name) as Location
```

**Search tags**
```
TASK FROM #cocktail
WHERE contains(text, "#cocktail")
```

**Not templates**
```
WHERE !startswith(file.path, "templates")

```

## DataviewJS
All examples should be in a `dataviewjs` code block.

**Use field from current page**
```
dv.current().fieldname
```

**Show fields in current page**
```
dv.paragraph(dv.current());
```

# Questions
