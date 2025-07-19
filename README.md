Commands Of GIT:

git init -> To initialize empty git Version control system(VCS) repo

git status -> to check whether a file is tracked, untracked or staged, also to check in which branch we are right now.

git add <file_name> -> To change a file from untracked to staged (Green), Untracked file will be in red 

git rm --cached -> To bring the file back to untracked if it is staged

git add . -> Move all the files which are untracked to staged

git commit -m "message" -> To track the files which are in staged

git restore <file_name> -> Restore a tracked file to its last committed state.

To push a file from local(your PC) to repository in github, create a repository in github ( In the background it used git init), To access the github from local we need a Personal access token( settings->developer setting-> generate new token-> Classic-> give repository access). if we create a repository in github its branch will be main, if you do it local, the branch will be master.

git remote set url origin https://(add your PAT)@github.com/(Your github username)/(Your repository name).git

git push origin master -> The file is now moved from local to github

What is Fork?: A copy of a repository.

To get a file from github to local, we need to clone the repo using: git clone <URL of the github reop>

To get a file from local to github it is git push, from github to local it is git pull

git branch -> Listing all the branch in our repo

git branch <branch_name> -> For creating a new branch

git switch <branch_name> or git checkout <branch_name> -> To switch to a different branch

git log  -> we can check head which is the latest commit in the current branch

If you want to merge the branches navigate to pull request tab in the github repo home page, base branch is the branch where we want the branch to be merged, compare branch is the branch we are merging to base branch.

git fetch -> will get all the branches from remote to local

Suppose, we have a file which has been pushed to the repo if we want to add any checks before it gets pulled we can do it by adding github-hooks. navigate to the .git directory in the local and enter into hooks directory, create a new file called pre-commit hooks. To check for errors in the python we can intsall flake8 and write the shell scripting cmd to check the conditions required.




