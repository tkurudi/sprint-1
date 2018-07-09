command line is like the nervous system, it can control everything.
search (regex)
git grep "regex"
list all branches
git branch -a
list remote branches
git branch -r
checkout an branch on remote
make sure you don't use origin

git fetch
git checkout branchName
Create a new branch
first create a branch

git checkout -b <branchName>
Create a new branch from an existing branch

git checkout origin/branchName -b newBranchName
Then push your new branch to the repo

git push origin <branchName>
Create a branch from a commit
AKA Recover a deleted branch

git checkout -b <branch> <sha>
revert all changes in a branch. Removes staged and working directory changes.
git reset --hard
Resets index to former commit; replace 56e05fced with your commit code. You can use git log to get commit code
git reset 56e05fced
revert a file to the most recent commit
git checkout HEAD -- /somePath/file.txt
undo the last commit. Blow it out of the water.
git reset --hard HEAD~1
undo your last commit but leave the files from that commit staged.
git reset --soft HEAD~1
delete local (untracked) files
git clean -f
If you want to also remove directories, run
git clean -f -d
to discard changes in working directory
git checkout -- <file>
Checkout a file from another branch
git checkout origin/branchName  -- fileName.txt
clean a folder
git clean -fxd {dir_path}