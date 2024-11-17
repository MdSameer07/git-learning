# git-learning

Learning-1

If two commit histories are not related
- git push -u origin main
- git push -u origin b1

Then use the below command to merge in those two commits into a new commit
- git merge --allow-unrelated-histories b1

Then for interactive rebasing do
- git rebase -i --root
squash the 2nd commit that you did as part of branch b1
update the commit message, this will still be the first commit
then do 
- git push origin main --force

Now you can only see one log in the commit log history

Learning-2

To revert back the unstaged changes
- git restore <file-name>

To revert back the staged changes
- git reset HEAD <file-name>

To revert back the commited changes
- git restore --source=<commit-hash> <file-name>

Learning-3

Accepting b1 change
- Before
- - Main, b1 branch changes
- After
- - Main, b2 branch changes, b1 branch changes, after rebasing with b2
- - Head -> b1

Accepting b2 changes
- Before
- - Main, b1 branch changes
- After
- - Main, b2 branch changes
- - Head -> b1, b2

Learning-4

git cherry-pick is similar to git rebase but differ in a way that rebase basically takes in all the commits from the source branch and applies them on top of the current branch's commit
while cherr-pick just takes in the commit that we want to apply on top of our branch's commit.

Learning-5

git clean -f - To clean all untracked files in current directory

git clean -fd - To clean all untracked files and directories

git clean -n - Dry run of clean to see which files and directories will be cleaned