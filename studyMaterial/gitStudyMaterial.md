Federica Cabrera Git Study Material:
VERSION CONTROL SYSTEMS

Repo hosting services

GIT / GITHUB
Git: It lets you and others work together on projects from anywhere. Git is a content tracker, can be used to store content. The code stored keeps changing as more code is added (many developers can add code in parallel), but Git maintains a history of what changes have happened. The code is not just stored in a central server, but the full copy of the code is present in all the developers’ computers.  Git keeps track of every modification to the code in a database, if something breaks, you can turn back to an earlier version or just compare the changes.

GitHub is just a hosting service that let you manage Git repositories, it serves as a location for uploading copies of a Git repository. 

Most common commands Commands:
git init [repository name] : initializes an empty Git repository in specified directory
git clone [url]: clones a repository located at an existing URL onto local machine, original repository can either be local or remote.
git status: to check the status of my repository, it lists all the files that have to be committed
git config: It sets the author name and email address to be used with your commits
git config -global user.name “[name]”
git config -global user.email “[email address]”
git add:
git add [file]: to add a file to the staging area, which allows them to be tracked
git add* : it adds one or more files to the staging area
git commit -m ”[message]”: it records in the local repository the changes made to the files. It should include a message explaining the changes made. Each commit has an unique ID
git commit: 
git commit -m “[message]”: this command records or snapshots the file permanently in the version history (it includes a message)
git commit -a :it will commit any files you´ve added with the git add command and also commits any files you´ve changed since then.
git diff: It shows the file differences which are not yet staged
git diff --staged: it shows differences between the files in the staging area and the latest version present.
git diff [first branch][second branch]: it shows the differences between the two branches mentioned.
git reset: 
git reset [file]: it unstages the file, but it preserves the file contents.
git reset [commit]: it undoes all the commits after the specified commit, and preserves the changes locally
git reset --hard [commit]: it discards all history and goes back to the specified commit
git pull [repository link]: it merges changes on the remote server to your working directory.
git push: 
git push [variable name] [branch]: this command sends the branch commits to your remote repository 
git push -all [variable name]: it pushes all branches to your remote repository 
git push [variable name] : [branch name]: it deletes a branch on your remote repository
git rm [file]: to delete a file from your working directory and stages the deletion
git stash: 
git stash save: it stores temporarily all the modified tracked files
git stash pop: it restores the most reset stashed files
git stash list: it lists all stashed changesets
git stash drop: it discards the most recently stashed changesets
git log: used to list the version history for the current branch
git log --follow[file]: lists version history for a file
git show [commit]: it shows the content changes of the specified commit
git tag [commitID]: used to give tags to the specified commit
touch: (+ name of the file to be created) to create a new file 
git checkout:
git checkout [branch name] : used to switch from one branch to another 
git checkout -b [branch name] : it creates a new branch and also switches to it
git branch: it lists all the local branches in the current repository
git branch [branch name]: it creates a new branch  
git branch -d [branch name]: it deletes the specified branch 
git merge [branch name]: it merges the specified branch´s history into the current branch
git remote add [variable name] [remote server link]: used to connect your local repository to the remote server


Rebase vs merge:
'Rebase compresses all the changes into a single 'patch'. Then it integrates the patch onto the target branch. Unlike merging, rebasing flattens history. Transfers the completed work from one branch to another. Unwanted history is eliminated.'

to create a new branch (a branch is like creating a parallel timeline, if you have two branches you can travel through them and add and commit things in parallel, when a new commit is made, the branch will move with it) 


If im checking a commit (and it has a branch)  and I commit sth => the commit will be added to the commit i was checking, the branch will stay where it was. But if im checking a branch and I commit sth => the commit will be added and the branch will “grow with it”

Git flow:
Git flow involves isolating your work into different types of branches. 
Flow workflow:
In the Git flow workflow, there are five different branch types:
Main:
The purpose of the main branch in this workflow is to contain production-ready code that can be released. It´s created at the start of a project and it´s maintained throughout the development process. Can be tagged at various commits in order to signify different versions or releases of the code. other branches will be merged into the main after testing and approval.
Develop:
The develop branch is created at the start of a project and is maintained throughout the development process (like main). Contains pre-production code with newly developed features that are in the process of being tested.
Feature:
Feature branch is a supporting branch. Is the most common type of branch in the git flow workflow. It is used when adding new features to your code. It´s started from the develop branch, and then merged when the feature is completed and properly reviewed. 
Release:
Release branch should be used when preparing new product releases. The base of the release branch, is the develop branch. The work being performed on release branches concerns finishing touches and minor bugs specific to releasing new code. 
Hotfix:
This branch is used to quickly address necessary changes in the main branch. The base of the hotfix branch should be the main branch, and should be merged into both the main and develop branches.

GitHub flow:
GitHub flow is simpler that Git flow.

Anything in the main branch is deployable 
To work on something new, create a descriptively named branch off of a master 
Commit that branch locally and regularly push your work to the same named branch on the server
When  you need feedback or help, or you think the branch is ready for merging, open a pull request
After someone else has reviewed and signed off the feature, you can merge it into master
With GitHub you can deploy from a branch for final testing in production before merging to main
Once your pull request has been reviewed, you can deploy your changes, if there´s some issue, you can roll it back by deploying the existing main branch into production.
Once changes have been verified in production, it is time to merge your code into the main branch (everything in the main branch is deployable) 

Trunk based development
Very similar to GitHub Flow, the crucial difference is where the release is performed from. Trunk-Based Development suggests deployment after production code is merged to the main branch to minimize chances for regression. 




