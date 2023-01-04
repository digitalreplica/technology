---
tags: a/note
---
in:: [[technology]]

# Notes
Markdown is a plain text document format.

## Github Markdown
Paragraphs **must** be double spaced (blank line between paragraphs), otherwise turns into a single-line, run-on mess.

Like this.

### Guides
* [Writing and formatting on GitHub](https://docs.github.com/en/github/writing-on-github/about-writing-and-formatting-on-github)
* [Mastering markdown](https://guides.github.com/features/mastering-markdown/)
* [about-readmes](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/about-readmes)

### Tools
[Gitdown](https://github.com/gajus/gitdown) looks interesting to preprocess markdown

### Relative links
Relative links can be used between any two documents, like `[Relative link](../hacking/aws.md)` becoming [Relative link](shared/hacking/aws.md). It's going to be a bit annoying to maintain.
* Hard to manually calculate going from one folder to another. Easier in atom with  [a plugin](atom.md). Spaces in filenames need `%20`s instead
You can "Copy relative path" in Atom, but that's only from the root directory down. Will have to manually add enough "../"s to go from the current folder up to the root.
* When changing a filename, or moving a file, will have to find all relative links to the page.

### Tables
GitHub markdown does support tables. [Working with Tables in GitHub Markdown | Pluralsight](https://www.pluralsight.com/guides/working-tables-github-markdown).

Example
| Header 1  | Another header here | This is a long header |
| --------  | ------------------- | --------------------- |
| Some data | Some more data      | data                  | 
| data      | Some long data here | more data             | 

# Reference
Markdown cheatsheets
https://github.com/adam-p/markdown-here
