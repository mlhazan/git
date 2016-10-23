# git

1. Add a folder to remote(When no README.me was added during the repo you made in the github website):

echo "# git1" >> README.md (or) create a file or folder then type: git init .
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:mlhazan/git1.git
git push -u origin master


2. cloning a repo:
git clone https://github.com/mlhazan/[nameOfRepo]/

3. push an existing repository from the command line

git remote add origin git@github.com:mlhazan/[nameOfRepo].git
git push -u origin master


4. remove or drop previous commits:

$ git rebase -i HEAD~3

find which commit you like to change:

pick e499d89 Delete CNAME
pick 0c39034 Better README
pick f7fde4a Change the commit message but push the same commit.

# Rebase 9fdb3bd..f7fde4a onto 9fdb3bd
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out

REMOVE pick with reword/drop 
PRESS esc in the keyboard
TYPE : ":wq"(EXCLUDE THE "")
PRESS ENTER

Force-push the amended commits:
git push --force

