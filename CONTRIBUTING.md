# Contributing to XXXX

<!-- Describe the aims of your package -->


## Key values

**Usability** and **maintainability** are the key elements every
contributor should have in mind. Do not forget that PR reviewers are the
gate-keepers: be thorough when writing code, be thorough when reviewing code
from other team members.

**Usability** is about building intuitive and robust API. A neat documentation
is mandatory, and includes in particular:

- updating the Changelog to highlight major feature additions and evolutions
- writing class- and function-level docstrings
- picking meaningful module, class, function and variable names

**Maintainability** is about ensuring our capability to improve and update the
codebase on the long-term. Beyond documentation, extensive testing is mandatory.
Writing a clean and understandable `git` history is also critical, and includes
in particular:

- Naming branch and PR with JIRA ticket name to enable JIRA and Github integration
  * `git checkout -b JRA-123-<branch-name>`
- writing meaningful commit messages with the Smart Commits syntax
  * `git commit -m "JRA-123 <summary of commit>"`
  * commit messages should start with a one-line summary
  * commits should be complete: consider `squash`-ing commits before merging
    your branch
- keeping the history linear, by `rebase`-ing before merging branches
- designing meaningful tests, with intuitive names or proper documentation

Please refer to the [Smart Commits
documentation](https://support.atlassian.com/bitbucket-cloud/docs/use-smart-commits/).

## Set VS CODE configuration

To maintain code quality and ease developers contribution, we provide a minimal
vscode settings.

In each new repository, please make sure to include these settings by:

* creating a `.vscode` folder
* adding the default [ruff
  configuration](https://github.com/epigenelabs/.github/blob/master/VSCODE_SETTINGS/ruff.toml)
* adding the [VSCode
  settings](https://github.com/epigenelabs/.github/blob/master/VSCODE_SETTINGS/settings.json)


# A fault confessed is fully redressed

As humans, we all do mistakes. It may (and it will) happen that bugs are merged
despite the tests and PRs, and that incomplete or buggy versions are released.

For the sake of usability and maintainability, the correct course of action in
such situations is to issue a fix, properly documented. Create a new PR with
name "fix for feature XX", and/or release a new version with a "fixed feature
XX" in the Changelog.

Users and fellow devs will forgive your mistake if you admit it, and will
gladly help to fix it. They will **NOT** forgive your trying to hide mistakes.
