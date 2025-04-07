### Push and Pull Repository  
To start working with a project, either one you've created or someone else had created, we can clone the repository and link it to a ssh key so we can interactively edit it and quickly push updated back to github.


To add update and/or new items to directory, we can use the interactive version of git add.
```
git add -i
git commit -m "some comment here"
git push origin branch_name
```


To pull edits from repo
```
git pull origin branch_name
```


random:
Upload changes:
```
Git add -I
Git commit -m "comment"
Git push origin main/branch_name
```

To work with ssh keys
```
Git clone rep_name
Git remote rm origin
Git remote add origin shh_key_from_github
```

To start new branch and migrate to it

To go beteen branches
```
Git checkout branch_name
```


Divergent branches:
hint: You have divergent branches and need to specify how to reconcile them.
If you just had a commit on origin but forget to pull before commiting something else locally, but got no conflicts, this one (a simple rebase) will solve it for you

```
git pull origin main --rebase
```

When merging, you may be asked to make a comment.
```
# To edit the editor:
:wq
```

When rebasing fails: reference [link](https://stackoverflow.com/questions/23517464/error-cannot-pull-with-rebase-you-have-unstaged-changes).
```
# If you try to push this error
❯ git push origin main
To https://github.com/DanielleMStevens/git_repo.git
 ! [rejected]          main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/DanielleMStevens/git_repo.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

# and try to rebase and get this error
❯ git pull origin main --rebase
error: cannot pull with rebase: You have unstaged changes.
error: please commit or stash them.

# instead try to autostash using the below command
git pull --rebase --autostash
```


