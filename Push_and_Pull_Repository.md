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
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.


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

If you try to pull and get this kind of error:
```
❯ git pull origin main
remote: Enumerating objects: 178, done.
remote: Counting objects: 100% (4/4), done.
remote: Total 178 (delta 4), reused 4 (delta 4), pack-reused 174 (from 1)
Receiving objects: 100% (178/178), 191.91 MiB | 174.00 KiB/s, done.
Resolving deltas: 100% (58/58), completed with 4 local objects.
From https://github.com/DanielleMStevens/repo_name
 * branch              main       -> FETCH_HEAD
error: cannot lock ref 'refs/remotes/origin/main': is at c8cb1afaa72699e61fe9a6144bd388a977a74e65 but expected 06381f3c69bf52b0f394dadbee3a61ebc9379beb
 ! 06381f3c..c8cb1afa  main       -> origin/main  (unable to update local ref)

# Then run:
git update-ref -d refs/remotes/origin/[branch-name]
git pull origin [branch name]
```



