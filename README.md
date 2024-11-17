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