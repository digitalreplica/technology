# Git

## Using a Template Repo
In Web UI, go into the repo, click "Use this Template" button

## Finding the number of commits for a given file
Returns one line per commit
```
git log --pretty=oneline -- <filename>
```
```
git log --oneline -- <filename>
```
## Make template repo
* Under Settings

https://docs.github.com/en/enterprise-server@3.1/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/creating-a-template-repository

## Git submodules
Links two repos together
```
git submodule add <url>
```

By default, the submodule is a directory with the repo name. That can be changed, by adding an optional folder name.
```
git submodule add <url> <local-dirname>
```

Updating all submodules
```
git submodule update --remote
```

[Git - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
