is:: [[note]]
from:: [[technology]]

# Notes
GitHub is an online [[git]] service provide

# Web-based Editor
Github has an IDE built in. Access it using:

    Pressing the dot ( . ) key while browsing any repository on GitHub.
    Change the URL from "github.com" to "github.dev".

[Web-based editor - GitHub Docs](https://docs.github.com/en/codespaces/developing-in-codespaces/web-based-editor#how-to-use-the-web-based-editor)

# Create user access token
* [Creating a personal access token - GitHub Docs](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token)

# Special files
Descriptions of the special files GitHub supports in a repo.
https://github.com/joelparkerhenderson/github-special-files-and-paths

# Special profile repos
Creating a repo with the same name as a GitHub username is a special repo. GitHub displays the Readme.md in the user's profile.

## License files
[licensing-a-repository](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
- license text in a file named `LICENSE.txt` (or `LICENSE.md` or `LICENSE.rst`)
- `LICENSE` also works

# GitHub actions
A CI/CD pipeline for GitHub. Action are stored in the repo as `.github/workflows/my-action.yml` files.

## Getting Started
* [Quickstart for GitHub Actions - GitHub Docs](https://docs.github.com/en/actions/quickstart)

## Sample workflows and actions
* [GitHub Marketplace · Actions to improve your workflow · GitHub](https://github.com/marketplace?type=actions)
* [GitHub - actions/starter-workflows: Accelerating new GitHub Actions workflows](https://github.com/actions/starter-workflows)

## Node.js actions
* https://github.com/actions/toolkit

## Python actions
* https://help.github.com/en/actions/language-and-framework-guides/using-python-with-github-actions

## Actions that commit
Actions can commit back to the repo they're run on. For workflows that trigger on push, this could cause infinite loops. Adding a `[skip ci]` or similar message in the commit will skip any workflows for that commit.

* [GitHub Actions: Skip pull request and push workflows with skip ci | GitHub Changelog](https://github.blog/changelog/2021-02-08-github-actions-skip-pull-request-and-push-workflows-with-skip-ci/)
* [Commit the result of a Github Actions job to its repository · GitHub](https://gist.github.com/anshumanb/16bf5e89354485f37912888d04d1be42)

## Disabling a step
Add ```if: ${{ false }}``` to the step

## Setting environment variable if file exists
```
run: (test -f ${{ env.REPO_LIST_PATH }} && echo "REPO_LIST_EXISTS=true" >> $GITHUB_ENV) || echo "REPO_LIST_EXISTS=false" >> $GITHUB_ENV
```

# GitHub CLI
* [GitHub CLI | Take GitHub to the command line](https://cli.github.com/)

Getting notes repos: ```gh repo list ${owner} --public --topic notes --json url --jq '.[]|.url'```

Cloning repo: `gh repo clone ${repo_name}`
```

Get note repos markdown urls: ```gh repo list <organization> --public --topic notes --json nameWithOwner,url,description --jq '.[]|"["+.nameWithOwner+"]("+.url+"): "+.description'```

Get fields available for a repo
```
gh repo view --json
```

Getting info for current repo
```
gh repo view --json name,nameWithOwner,owner,url,updatedAt
```

With a template
```
gh repo view --json name,url --template '{{printf "name: %s\nurl: %s\n" .name .url}}'
```

Clone all repos:
* use https://github.com/matt-bartel/gh-clone-org extension
```
gh clone-org <organization>
```

Sync a single repo
```
cd repo
gh repo sync
```

# GraphQL
Explorer
* [GitHub GraphQL Explorer](https://graphql.github.com/)

Making queries
* [Using Github’s GraphQL to retrieve a list of repositories, their commits and some other stuff — part 1 | by Fábio Molinar | Medium](https://medium.com/@fabiomolinar/using-githubs-graphql-to-retrieve-a-list-of-repositories-their-commits-and-some-other-stuff-ccbbb4e96d78)

# GitHub Organizations
Organization profile
* [Customizing your organization’s profile - GitHub Docs](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)

## Using GitHub Organizations to organize repositories
[How I Organize my GitHub Repositories | by Andrei Cioara | Andrei Cioara](https://andreicioara.com/how-i-organize-my-github-repositories-ce877db2e8b6)
* Use github organizations to group repositories together

# GitHub Markdown
## Table of Contents
Github automatically generates a table of contents if there are 2 or more headings. Access in tiny dropdown beside filename.
* [Table of Contents support in Markdown files | GitHub Changelog](https://github.blog/changelog/2021-04-13-table-of-contents-support-in-markdown-files/)
