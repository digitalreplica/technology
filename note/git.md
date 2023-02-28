is:: [[note]]
from:: [[technology]]
near:: [[github]]

# Notes
Git cli notes.

# Howto
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

## Squashing commits in main branch
- https://docs.github.com/en/desktop/contributing-and-collaborating-using-github-desktop/managing-commits/squashing-commits


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

Removing submodules. From [git - How do I remove a submodule? - Stack Overflow](https://stackoverflow.com/questions/1260748/how-do-i-remove-a-submodule), modern git versions allow
```
git rm {submodule}
git config --remove-section submodule.{submodule}
```

# Resources
* [Git - Book](https://git-scm.com/book/en/v2)


# Older Howto
**git clone**
```
git clone https://repository
```
  

**create repo**
```
git init
```
  
**Basic updating**
````
git fetch git merge -or- git pull
````

**Renaming a file**
```
git mv old_filename new_filename
```

  
**Resetting**

If you instead want to drop all your local changes and commits, fetch the latest history from the server and point your local master branch at it like this
```
git fetch origin
git reset –hard origin/master
```

**Create a branch**
```
git branch git checkout -or- git checkout -b 
```

**Updating a branch**
```
git commit -a -m “message” git push origin 
```
  

**To delete local branches which have already been merged into master:**
```
git branch –merged master | grep -v “* master” | xargs -n 1 git branch -d
```
  

**To create a local and remote repo using the local filesystem**
```
git init –bare myrepo.git
cd myrepo
git init
git remote add origin /home/user/Documents/myrepo.git/
git add -A
git commit -m “initial repo” git push origin master
```
  

**To merge master into a branch via merging (preferred way)**
```
git checkout master
git pull
git checkout branch
git merge master
```
  

**To merge master into a branch via rebasing (cleaner way, but not preferred cause it rewrites history)**
```
git checkout master git pull git checkout branch git rebase master
```

**To pull a single file from master into a branch (reset a single file)**
```
git checkout origin/master my/filename
```
  

**To ignore local changes for certain files**
```
git update-index –assume-unchanged my/filename
```
  

**To save a file temporarily (like maybe passwords)**
```
git stash git stash list
``` 

**Diff a stash**
```
git diff stash@{0}
```
Reverting a commit Probably the best way to undo a single commit. Makes a new commit with the changes stripped out. git revert 

 
**Merging a specific file from a branch into master**
```
git checkout master git pull git checkout branch-name path/to/file git add -A git commit -m “merge file from branch” git push
```

## Diff
**Diffing between current and master**
```
git diff master
```

**Diffing between current and the last commit**
```
git diff HEAD^ HEAD
```
