### Push and Pull Repository  
To start working with a project, either one you've created or someone else had created, we can clone the repository and link it to a ssh key so we can interactively edit it and quickly push updated back to github.


To add update and/or new items to directory, we can use the interactive version of git add.
```
git add -i
```

To add a comment to the commit 
```
git commit -m "some comment here"
```

To push to current branch
```
git push origin branch_name
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
