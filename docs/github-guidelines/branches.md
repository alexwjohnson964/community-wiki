---
sidebar_position: 3
---

# Github branches for source and forked repos

Branches in Github are copys of the current repository that are directly linked to the existing repository that allow for changes to be made that do not affect other branches in the repository.

For this community we will be using a set of standardized branch names in order to better understand what each branch is designed to do and are outlined as follows:

Source reopositories (Owner is the organization):
- `main`: The production branch of the project which will contain the current working version of the project that is served to users
- `<version>-dev`: The development branch for the next version of the project where pull requests from forks will be merged into. When a version is complete the development branch will be merged into `main` and a new development branch for the next major version will be created
    - Example: `1.0.0-dev`

Fork repositories (Owner is a contributor):
- `main`: A copy of the source repo's production branch which will need to be regularly synced in order to maintain consistency across all forks of the project
- `<issue-number>-<issue-description>`: issue specific branches that are used for developing changes that will be later merged into the source repository
    - Example: Implementing issue number `1` with description `create login page` has a branch named something like `1-login-page`

These methods of branch management will ensure that everyone knows what different branches contain and where to merge changes into as development on different projects progresses.

To create new branches please use the [checkout](../git-commands/checkout.md) git command.