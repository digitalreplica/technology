# GitHub

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

# GitHub actions
A CI/CD pipeline for GitHub. Action are stored in the repo as `.github/workflows/my-action.yml` files.

## Getting Started
* [Quickstart for GitHub Actions - GitHub Docs](https://docs.github.com/en/actions/quickstart)

## Sample workflows and actions
* [GitHub Marketplace · Actions to improve your workflow · GitHub](https://github.com/marketplace?type=actions)
* [GitHub - actions/starter-workflows: Accelerating new GitHub Actions workflows](https://github.com/actions/starter-workflows)

## Python actions
* https://help.github.com/en/actions/language-and-framework-guides/using-python-with-github-actions

## Actions that commit
Actions can commit back to the repo they're run on. For workflows that trigger on push, this could cause infinite loops. Adding a `[skip ci]` or similar message in the commit will skip any workflows for that commit.

* [GitHub Actions: Skip pull request and push workflows with skip ci | GitHub Changelog](https://github.blog/changelog/2021-02-08-github-actions-skip-pull-request-and-push-workflows-with-skip-ci/)
* [Commit the result of a Github Actions job to its repository · GitHub](https://gist.github.com/anshumanb/16bf5e89354485f37912888d04d1be42)

# GitHub CLI
* [GitHub CLI | Take GitHub to the command line](https://cli.github.com/)

# GraphQL
Explorer
* [GitHub GraphQL Explorer](https://graphql.github.com/)

Making queries
* [Using Github’s GraphQL to retrieve a list of repositories, their commits and some other stuff — part 1 | by Fábio Molinar | Medium](https://medium.com/@fabiomolinar/using-githubs-graphql-to-retrieve-a-list-of-repositories-their-commits-and-some-other-stuff-ccbbb4e96d78)