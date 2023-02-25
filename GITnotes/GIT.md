# Git Fundamentals

### What is version control?
Version control, also known as source control, is the practice of tracking and managing changes to software code.
Version control systems are software tools that help software teams manage changes to source code over time.

###### For anyone who creates content
* Remembers each version update
* Provides a history of all changes
* Can go back to an early version

##### Can provide off-site copy of data
* Easy synchonisation with local copy

##### Supports collaboration
* People may update simultaneously
* Might make overlapping changes
* Can support merging and dealing with conflicts

### What is Git?
* Git is a version control system
* Fast, modern, fully featured
* Easy to learn and most popular 
* Open source and free
* Provides version history
* Great for collaborative work in teams
* Distributed: Local copy of data, optional remote copy

### What is provided with Git?

##### Git comes with a command-line user interface
* Git Bash
* All commands can be run through this UI

##### Git server can be used to copy data
* Included with Git
* Most people use an Internet solution
* Pupular options GitHub, GitLab, BitBucket

##### Graphical UI can also be used 
* GitHub Desktop and ID integration

##### A directory/folder controlled by Git is called a "repository"
* "Repo"

### Git commands
* git init: create new git repository
* git clone: similar to git init
* notepad .gitignore: excludes files when pushing to git server
* git remote add origin "url of repo": add the repo from server to the staging area
* git pull origin master(main branch): pull repo from server
* git status: check untracked files, commits and branch you are currently in
* git add .: add all untracked files to staging area
* git add "file name": add specific file to staging area
* git commit -m "message": summaries which version to be uploaded to the server
* git push origin master(main branch)
* git log: list commits
* git diff: show changes between 2 files
* git checkout: restore changes

##### What does git init do?
* Creates .git folder
* Stores config information for the repo
* Remembers all history
* Versions of all the files
* All branches
* Keeps track of where you are currently working