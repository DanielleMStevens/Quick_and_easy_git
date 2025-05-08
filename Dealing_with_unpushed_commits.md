Use this version:

    ```
    # 1. Undo the most recent commit, keeping the changes staged:
    git reset --soft HEAD~1
    
    # 2. Check the status (optional, for verification):
    git status
    
    # 3. Unstage the problematic large files:
    git reset HEAD ./07_model_results/04_random_esm2_with_receptor_05_datasets/checkpoint-19.pth
    git reset HEAD ./07_model_results/04_random_esm2_with_receptor_05_datasets/checkpoint-9.pth
    # (Repeat for any other large files in that commit)
    
    # 4. Once all oversized files are unstaged, create a new commit:
    git commit -m "Remove large model checkpoints and update commit"
    
    # 5. Push the corrected commit to your branch:
    git push origin your_branch_name
    ```


Version 1: Delete the most recent commit, keeping the work you've done:

    git reset --soft HEAD~1
    git status
    git reset HEAD ./path/to/problem/file

    # once all files are unstaged
    git commit -m "comment about issue"
    git push origin branch_name

See this link: https://builtin.com/software-engineering-perspectives/git-reset-soft-head

Version 2: Delete the most recent commit, keeping the work you've done:

    git reset --soft HEAD~1
    git commit --amend -CHEAD
    git push --set-upstream origin main

https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github

Remove the files from the git index but keeping in the working directory

    # monitor file stauts
    git status --cached path/to/file

    # remove each file which is causing the conflict
    git rm --cached path/to/file

    # then issue a new Commit and Push


https://stackoverflow.com/questions/348170/how-do-i-undo-git-add-before-commit
https://stackoverflow.com/questions/33610682/git-list-of-staged-files


Delete the most recent commit, destroying the work you've done:

    git reset --hard HEAD~1

This command will sync the local repository with the remote repository getting rid of every change you have made on your local. You can also do the following to fetch the exact branch that you have in the origin.

    git reset --hard origin
    git reset --hard origin/<branch>

Data can also be recovered: https://stackoverflow.com/questions/25791533/unstaged-files-gone-after-git-reset-hard


Remove files from your git repositiory but keeping in your local directory

https://docs.github.com/en/repositories/working-with-files/managing-large-files

