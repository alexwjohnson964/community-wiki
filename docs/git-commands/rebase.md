---
sidebar_position: 10
---

# Rebase

The git rebase command allows for the restructuring of the commit history between a local repository branch and remote repository branch such that all of the remote repository commits come first and any that are not in the remote repository branch but are present in the local repository branch are placed after.

This command is most useful when changes have been made to the remote repository `main` branch that need to be reflected in a development branch for new features in order to maintain a clean and linear commit history.

This command can also be used between two branches in the same local repository but for community projects it is unlikely that this command will need to be used for that situation.

## Basic Rebase

To perform a basic rebase to move the active local branch commits on top of another remote branch use:

`git rebase <remote-name>/<remote-branch-name>`

Where `<remote-name>` is the name of the linked remote repository found with the [remote](./remote.md) command and `<remote-branch-name>` is the name of the branch in the remote repository that is being rebased on top of.

## Interactive Rebase

For most rebases there will be merge conflicts that will need to be addressed during the process; to simplify this process it is recommended to use the `-i` flag to perform the rebase in interactive mode:

`git rebase -i <remote-name>/<remote-branch-name>`

Where `<remote-name>` is the name of the linked remote repository found with the [remote](./remote.md) command and `<remote-branch-name>` is the name of the branch in the remote repository that is being rebased on top of.

In the interactive mode you can make a number of actions on each commit as it is rebased:
- `pick`: Keep the commit as is
- `squash`: Combine commits together
- `edit`: pause to change a commit
- `reword`: change just the commit message

Use the following steps when performing an interactive rebase:
1. Edit the commit message or choose an action (pick, squash, edit, reword)
2. Save and close the editor
3. Git will apply the changes and let you review the results

## Continue a rebase

If there is a conflict that needs to be addressed during the merge process in non-interactive mode then make any neccessary changes before using the `--continue` flag to continue the rebase:

`git rebase --continue`

## Abort a rebase

If something goes wrong and you want to cancel the rebase for any reason use the `--abort` flag:

`git rebase --abort`

This will cancel the rebase and return the branch that was being changed back to its starting condition.

## Skip a commit in a rebase

If there is a conflict during the rebase process that cant be resolved or for if any reason there is a commit that should not be rebased onto the branch then use the `--skip` flag:

`git rebase --skip`

This will skip the current commit and move on to the next in the rebase process