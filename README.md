# Learn Git: A Cheat Sheet for Essential Git Functions

**T**here are many graphical implementations of Git, but original interactions were done via a **command line interface(CLI)**. These terminal commands are still very relevant and useful today, which is why I have created this small cheat sheet: to give beginner Git users a solid foundation of the commands they should know/be aware of.

Although this information can be found elsewhere online, I often found myself trawling through documentation pages and Stack Overflow answers to find some of the most basic commands. This cheat sheet aims to consolidate this basic information into one, accessible page that can help beginners get started in the world of version control and software development.

## VERSION CONTROL

Before Git, first we should know about Version Control. The system that tracks/records the changes made to the files or set of files over time so that we can be reverted back to a specific version at a later date is known as **Version Control**. Each and every modification is tracked. From addition of a single alphabet to removal of a whole section. There are many version systems but the most popular version control system is **Git**. 

Git is a distributed Version Control System, developed by **Linus Torvalds** in 2005. Git’s primary objective is to implement and design a version control system that was distributed, reliable and fast. It allows us to have the files locally. We don’t need any fancy servers to host the files. Git makes collaboration easier and seamless. Multiple team members can work on the same file of a project without ever disturbing the other person. Each team member can work independently and later on blend the best of each contributor’s effort to make the files and the project robust. But, you may question ***‘What about the conflicts that might arise with merging too many codes of the same project?’***. And this is where the feature of Git shines. Git or version control in general helps to resolve the conflict. Git offers powerful tools to help navigate and resolve conflicts. It handles the merges on its own with automatic merging features. But in situations where Git is unable to merge them, then it will mark the conflict and have you resolve it. 

The distributed part of the Git allows developers **clone** an entire repository onto their own machine. This allows for backups and there won’t be any single point of failure. Another feature of version control is that it enables the developer to work on multiple features of the project at the same time. This gives great scope for experimentation, trial and error. As each feature is developed independently of the others, it can easily be removed if it doesn’t work out. 

There is one more thing to add to the Introduction of Git. People often get confused between **Git** and **GitHub**. All things considered Git and GitHub aren’t the same thing. GitHub is a hosting site for Git projects or repositories. There are other solutions that provide services related to Git. Some of them are **Bitbucket** and **GitLab**. GitHub and Bitbucket are cloud-based solutions, but GitLab allows you to set up this functionality in their own servers. 


# COMMON TERMINOLOGIES

## Repository: 
    A unit of storage and change tracking that represents a directory of whose contents are tracked by Git.
    
## Branch
    A version of a repository that represents the current state of the  set of files that constitute
    a repository. In a repo, there exists a default or main branch that represents the single source of truth.
    
## Master
    It is the default or main branch. A version of the repository that is considered the single source of truth. 
    
## Reference
    A Git ref or reference is a name corresponding to a commit hash.
    The references are stored in a file .git/refs directory of the repository.
  
## HEAD
    A reference to the most recent commit on a branch. The most recent commit is commonly referred
    to as the tip of the branch.
   
## Working Tree
    This refers to the section in which we view and make changes to the files in a branch. 
    The files that are changed are then moved to a staging area once they are ready for a commit.
    
## Index
    This is an area where Git holds files that have been changed, added or removed in readiness
    for a commit. It’s a staging area from where you commit changes.
    
## Commit
    This is an entry into Git’s history that represents a change made to a set of files at a given 
    point in time. A commit references the files that have been added to the index and update the 
    HEAD to point to the new state of the branch.
    
## Merge
    It is a process of incorporating changes from one branch to another. In Git, other branch are 
    merged into the master branch.
    
    
  

