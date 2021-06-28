VERSION CONTROL SYSTEMS
Repo hosting services
GIT / GITHUB
Git: It lets you and others work together on projects from anywhere. Git is a content tracker, can be used to store content. The code stored keeps changing as more code is added (many developers can add code in parallel), but Git maintains a history of what changes have happened. The code is not just stored in a central server, but the full copy of the code is present in all the developers’ computers.  Git keeps track of every modification to the code in a database, if something breaks, you can turn back to an earlier version or just compare the changes.

GitHub is just a hosting service that let you manage Git repositories, it serves as a location for uploading copies of a Git repository. 
Most common commands Commands:
Basics:
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
Undoing changes
git revert [commit hash] : creates a new commit that undoes all of the changes made in [commit hash], and applies to the current branch.
git reset: 
git reset [file]: it unstages the file, but it preserves the file contents.
git reset [commit]: it undoes all the commits after the specified commit, and preserves the changes locally
git reset --hard [commit]: it discards all history and goes back to the specified commit
Rewriting git history
git commit --amend : replaces the last commit with the staged changes and last commit combined. Can be used with nothing staged, to edit the last´s commit message.
git rebase [base]: rebase the current branch onto [base] 
git reflog : show changes made to the local´s repository head
Git branches commands
git branch: it lists all the local branches in the current repository
git branch [branch name]: it creates a new branch  
git branch -d [branch name]: it deletes the specified branch

git checkout:
git checkout [branch name] : used to switch from one branch to another 
git checkout -b [branch name] : it creates a new branch and also switches to it

git merge [branch name]: it merges the specified branch´s history into the current branch

Remote repositories
git remote add [url] : creates a new connection to a remote repository
git fetch [remote][branch] : fetches a specific [branch] from the repository, if you don't add [branch], it fetches all remote refs. 
git pull [remote] : fetches the specified remote´s copy of the current branch and immediately merge it into the local copy 
git push [remote][branch] : push the branch to [remote] along with necessary commits and objects. Creates named branch in the remote repository if it does not exist.
Tagging
Git has the ability to tag specific points in a repository´s history as being important. You can mark release points such as v1.0, v2.0 and so on.

Listing existing tags:
git tag

Creating tags:
Git supports lightweight and annotated tags.

Lightweight tags are just like a pointer to a specific commit (does not contain annotations or messages). It will just point.

git tag v1.0 

Annotated tags are stored as full objects in the git database. Contain the tagger name, email and date; have a tagging message and can be signed and verified. 

git tag -a [anotation] : ej: git tag --a v1.0
 
Deleting taggs:
git tag --d [tag name]
Git stash
The git stash command takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy. The stash is local to your git repository and it is not transferred to the server when you push.

By default, git stash will stash:
Staged changes
Unstaged changes (tracked)
will not stash:
New files untracked
Deleting stash
git stash drop : deletes stash
git stash clear : deletes all stashes


Git Merge
Git merge is a command that allows you to merge branches from Git (history is preserved)
Git Rebase
Git rebase is a command that allows developers to integrate changes from one branch to another. 
Rebase compresses all the changes into a single “patch”. Then it integrates the patch onto the target branch. Unlike merging, rebasing flattens history. Transfers the completed work from one branch to another. Unwanted history is eliminated.

Similarities:
Git rebase and merge both integrate changes from one branch into another

Differences:
Git rebase moves a feature branch into a master, while git merge a new commit preserving the history.

Deciding merge or rebase:
Depends on the branching strategy. Git rebase makes sense for individuals, not so much for teams. (It is a matter of preserving or not all the history of the changes made)
Git squash:
To “squash” in Git means to combine multiple commits into one. There is no such thing as a stand-alone git squash command. Instead, squashing is rather an option when performing other Git commands like interactive rebase or merge. 

It would be a good idea to squash when you have too many commits, or you decide to squash before merging so all the individual commits from the feature branch will be combined to a single commit.

You can decide to preserve all the individual commits and avoid squashing, it´s just a matter of avoiding some unnecessary history.

Usage: 

git merge --squash : for merging

git rebase --s : for rebasing
Hooks:
Git hooks are scripts that run automatically every time a particular event occurs in a Git repository. For example you can set a hook that prevents you from committing if the hook detects a problem.   They are listed in the .git folder /hooks.

Pre-commit as a hook, for example, is executed every time you run git commit before Git asks the developer for a commit message or generates a commit object. It inspects the snapshot that is about to be committed. This script aborts the commit if it finds any error.

Other useful hooks: prepare-commit-msg, commit-msg (same as prepare-commit-msg but called after the user enters a commit message), post-commit (notification purposes), post checkout.
Git branching strategies:
A git branching strategy model provides the rules for how, when and why branches are created and named.
There are many popular branching strategies, choosing one depends on your team's environment, product and your specific development needs.
Git Flow:
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
GitHub Flow:
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



