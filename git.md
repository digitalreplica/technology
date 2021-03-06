# Git

## Common CLI commands
* List branches: ```git branch -a```

**Finding the number of commits for a given file**
* Returns one line per commit
```
git log --pretty=oneline -- <filename>
```
or
```
git log --oneline -- <filename>
```

**See if a repo has uncommitted changes**
```
git status --porcelain
```
or
```
git status -s
```

## Git-related tidbits
* Global .gitignore file: https://sebastiandedeyne.com/setting-up-a-global-gitignore-file/

## Templates
**Using a Template Repo**
In Web UI, go into the repo, click "Use this Template" button

**Make template repo**
* Under Settings

https://docs.github.com/en/enterprise-server@3.1/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/creating-a-template-repository

## Tagging
Checking: ```git log --oneline```

Create tag (locally): ```git tag -a <tag_name> -m "<Message_for_commit>" <commit_hash_code>```

Update tag (locally): ```git tag -f <tag_name_to_update> <hash_code_new_commit>```
* <hash_code_new_commit> default is HEAD if left blank

Push tags: ```git push --tags```

# Git submodules
Links two repos together
```
git submodule add <url>
```

By default, the submodule is a directory with the repo name. That can be changed, by adding an optional folder name.
```
git submodule add <url> <local-dirname>
```

Updating submodules, including empty ones
```
git submodule update --init
```

Updating all submodules. Does a `git fetch` and `git merge` on all submodules
* note: don't use `git submodule update --remote`, as it assumes a `master` branch by default
```
git submodule foreach 'git pull'
```

[Git - Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

Removing submodules is a horrible mess. First attempt wasn't fully successful, and ended up wiping the commit and repulling from main. Used the first answer in [git - How do I remove a submodule? - Stack Overflow](https://stackoverflow.com/questions/1260748/how-do-i-remove-a-submodule).

# Resources
* [Git - Book](https://git-scm.com/book/en/v2)
