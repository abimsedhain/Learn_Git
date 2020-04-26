# Learn Git: A Cheat Sheet for Essential Git Functions

This small cheat sheet was created to give beginner Git users a solid foundation of the Git command line interface commands that they should know/be aware of. There are other resources online but this sheet's aim is to consolidate this basic information into one, accessible page that can help beginners get started in the world of version control and software development.

## Version Control

**Version Control Systems (VCSs)** are the system that tracks/records the changes made to the files or set of files over time so that we can be reverted back to a specific version at a later date. Each and every modification is tracked. From addition of a single alphabet to removal of a whole section. It tracks changes to a folder and its contents in a series of snapshots, where each snapshot encapsulates the entire state of files/folders within the top-level directory. While other VCSs exist, Git is the de facto standard of version control.  

**Git** is a distributed Version Control System, developed by **Linus Torvalds** in 2005. Git’s primary objective is to implement and design a version control system that was distributed, reliable and fast. It allows us to have the files locally. We don’t need any fancy servers to host the files. Git makes collaboration easy and seamless. Multiple team members can work on the same file of a project without ever disturbing the other person. Each team member can work independently and later on blend the best of each contributor’s effort to make the files and the project robust. 

But, you may question ***‘What about the conflicts that might arise with merging too many codes of the same project?’***. And this is where the feature of Git shines. Git or version control in general helps to resolve the conflict. Git offers powerful tools to help navigate and resolve conflicts. It handles the merges on its own with automatic merging features. But in situations where Git is unable to merge them, then it will mark the conflict and have you resolve it. 

The distributed part of the Git allows developers **clone** an entire repository onto their own machine. This allows for backups and there won’t be any single point of failure. Another feature of version control is that it enables the developer to work on multiple features of the project at the same time. Different brances can created for the project and later on merged together. This gives great scope for experimentation, trial and error. As each feature is developed independently of the others, it can easily be removed if it doesn’t work out. 

There is one more thing to add to the Introduction of Git. People often get confused between **Git** and **GitHub**. All things considered Git and GitHub aren’t the same thing. GitHub is a hosting site for Git projects or repositories. There are other solutions that provide services related to Git. Some of them are **Bitbucket** and **GitLab**. GitHub and Bitbucket are cloud-based solutions, but GitLab allows you to set up this functionality in their own servers. 


# Common Terminologies

- **Repository**: A unit of storage and change tracking that represents a directory of whose contents are tracked by Git.
    
- **Branch**: A version of a repository that represents the current state of the set of files that constitute
    a repository. In a repo, there exists a default or main branch that represents the single source of truth.
    
- **Master**: It is the default or main branch. A version of the repository that is considered the single source of truth. 
    
- **Reference**: A Git reference is a name corresponding to a commit hash(SHA-1 Hash). References are pointers to commits. 
    Unlike objects they are mutable.
  
- **HEAD**: A reference to the most recent commit on a branch. The most recent commit is commonly referred to as the tip of the branch.
   
- **Working Tree**: This refers to the section in which we view and make changes to the files in a branch. The files that are 
    changed are then moved to a staging area once they are ready for a commit.
    
- **Index**: This is an area where Git holds files that have been changed, added or removed in readiness for a commit.
    It’s a staging area from where you commit changes.
    
- **Commit**: This is an entry into Git’s history that represents a change made to a set of files at a given point in time. 
    A commit references the files that have been added to the index and update the HEAD to point to the new state
    of the branch. And Commits in Git are immutable.
    
- **Merge**: It is a process of incorporating changes from one branch to another. In Git, other branch are merged into the 
    master branch.
    
        
# Git Command-Line Interface Commands    

## Initial Setup

 - `git init` : Initializes a existing directory as a Git Repo.
 - `git clone [URL]` : Creates a local copy of a remote Git Repo via URL.
 
 ## Staging
 
  - `git status` : Shows modified files in the local, working directory.
  - `git add [file]` : Adds a particular to next commit(stage).
  - `git add .` : Adds all the modified files to next commit(stage).
  - `git reset [file]` : Unstages a file while retaining the changes in local directory.
  - `git reset --hard` : Discards all local changes to all files.
  - `git diff` : Shows the changes to the unstaged files.
  - `git diff --staged` : Shows the changes to staged, but uncommited files.
  - `git commit -m [Descriptive message]` : Commits the stages content as a new commit snapshot.
  
## Branches

  - `git branch` : Lists all the branches. An asterisk will be next the active branch.
  - `git branch [branch-name]` : Creates a new branch at the current commit.
  - `git checkout [branch]` : Switches the branches, makes it the active branch.
  - `git merger [branch]` : Merges the specified branch to the current active branch.
  
## Inspection

  - `git log` : Shows the commit history for the current active branch.
  - `git log --follow [file]` : Shows the commits that changed file.
  - `git diff [branchB]....[branchA]` : Shows the diff of branchA to branchB.
  - `git show [SHA]` : Shows one or more objects (blobs, trees, tags and commits) in human readable form.
  - `git blame [file]` : Shows who changed what and when in a particular file.
    
## Sharing
  - `git remote -v` : Shows a list of configured remote repo's URLS.
  - `git remote add [alias] [URL]` : Adds a Git URL as a remote alias.
  - `git remote rm [alias]` : Removes a remote alias from the project.
  - `git fetch [alias]` : Fetchs down all the branches from a specified remote URL.
  - `git merge [alias]/[branch]` : Merges a remote branch into your current branch.
  - `git push [alias] [branch]` : Pushes local branch commits to the remote repo branch.
  - `git pull` : Fetches and merges any commit from the tracking remote branch.
  
## Rewrite and History
  - `git revert` : Reverts back to a specific point to undo changes to repo's commit history.
  - `git rebase [branch]` : Applies any commit of current branch ahead of specified one.
  - `git reset --hard [commit]` : Clears staging area and rewrites working tree from specified commit.
  
## Stashing
  - `git stash` : Saves modified and staged changes.
  - `git stash --include-untracked` : Saves the untracked files as well.
  - `git stash list` : Lists stack-order of stashed file changes.
  - `git stash apply` : Resumes working on the stash at the top of our stash list while keeping stash intact.
  - `git stash pop` : Resumes working on the stash at the top of our stash list and deletes the stash intact.
  - `git stash drop [stash-id]` : Deletes a specific stash.
  - `git stash clear` : Deletes all stashes.

