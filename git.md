# GIT

### What is the difference between git pull and git fetch?

git fetch only downloads new data from a remote repository - but it doesn't integrate any of this new data into your working files. 
git pull is shortcat for git git fetch and git merge.

### What is git stash?

Stash the changes in a dirty working directory away.
When you want to record the current state of the working directory and the index, but want to go back to a clean working directory. The command saves your local modifications away and reverts the working directory to match the HEAD commit

### Describe git rebase?

Rebase the current branch on top of the master branch


### How to make one out of three commits?
git rebase -i master (instead of master you can also use a specific commit)

Change 'pick' to 'squash'
Save changes


### Describe git merge strategies?

User can specify merge strategy using -s option with git merge and git pull commands.

- resolve (default)
This can only resolve two heads (i.e. the current branch and another branch you pulled from) using a 3-way merge algorithm. It tries to carefully detect criss-cross merge ambiguities and is considered generally safe and fast.

- recursive
This can only resolve two heads using a 3-way merge algorithm. When there is more than one common ancestor that can be used for 3-way merge, it creates a merged tree of the common ancestors and uses that as the reference tree for the 3-way merge. This is the default merge strategy when pulling or merging one branch.

- octopus
This resolves cases with more than two heads, but refuses to do a complex merge that needs manual resolution. It is primarily meant to be used for bundling topic branch heads together. This is the default merge strategy when pulling or merging more than one branch.

- ours
This resolves any number of heads, but the resulting tree of the merge is always that of the current branch head, effectively ignoring all changes from all other branches. It is meant to be used to supersede old development history of side branches.

- subtree
This is a modified recursive strategy. When merging trees A and B, if B corresponds to a subtree of A, B is first adjusted to match the tree structure of A, instead of reading the trees at the same level. This adjustment is also done to the common ancestor tree.