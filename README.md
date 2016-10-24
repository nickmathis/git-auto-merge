# git-auto-merge
Automerge branches

## Usage
`git-auto-merge target_branch list_of_branches`

`target_branch` is the merge branch (will be created, if needed)
`list_of_branches` is the list of branches, separated by a space, that you want to merge into `target_branch`


* Any branches that can be merged will be, and the rest skipped.
* Some output is provided to let you know how the command ran.
* `list_of_branches` is tried in order

### Security consideration
This runs with shell commands, so don't pass in malicious code. Plus this is probably running on your own machine, and you don't want to break that.

### To Do (maybe)
* Sanitize the branch names for shell execution
* Maybe switch to `git-ruby` gem for git interaction
* Implement some sort of smart-retry system to optimize merge conflicts
