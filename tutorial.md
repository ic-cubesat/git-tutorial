% git 101

# Version Control

## Collaborative Editing

### The problem
- One document, many editors
- How to allow editors to work in parallel?
- How to avoid overriding changes?
- How to keep track of changes?
- How to revert to previous versions of the document?

### The solution
- Version Control Systems!

## Architecture Of a Version Control System

![Centralized and distributed version control systems](images/cubesat-git-tutorial-arch.png)

# git

## About
<!-- # git -->

* git is an _implementation_ of a _distributed VC system_

* git provides:
    * server utilities
    * client utilities (command line, GUIs)

* git is widely used for open source development

* there are providers for free storage for public git repositories:
     * GitHub (the one we use)
     * Bitbucket
     * Google Code (?)

* a very good online resource -- http://git-scm.com/

<!-- # git -->

## Workflow

1. git clone - get a copy of the repository
2. make some changes
3. git status - check chagnes
4. git add    - stage changes
5. git commit - commit changes
6. git pull   - fetch other changes to the repository that happened in the meantime
7. git commit - commit the merged changes
8. git push   - push your changes
9. done!

# git command line client

## Getting Started

### Getting Help

* To get help on git --- `git --help`

* To get help on a command --- `git help <command>`

* Most commands work only inside a git repository

### Copying remote repository

`git clone <path/to/repository>.git`

### Seeing your changes

`git status`

<!-- # git command line client -->

## Saving Changes Locally

### Staging your changes

`git add <path/to/changed/file>`

* Staging means 'I am preparing to commit this work'

### Committing your work

`git commit -m <Useful message>`

* Commits all staged changes to your local repo
* Useful messages are helpful when reviewing change history

## Syncing your changes

`git pull -u <repo> <branch>`

* Means 'get all recent changes from repo and apply them to my local
  version'
* Often `<repo>` is origin, `<branch>` is master
* git can sometimes merge the local and remote versions automatically
* when this fails, the file is marked with `CONFLICT`
* when a file is marked with `CONFLICT` you need to edit it to ensure
  the correct version is selected (this may be tricky)
* when you are done, make a new commit -- you are now up to date
  (unless someone else just made some more changes...)

<!-- # git command line client -->

## Push & Check

### Uploading your local copy

`git push -u <repo> <branch>`

* Pushes your changes to repo on branch
* You must have done a `pull` beforehand

### Viewing the change history

`git log`

* shows a history of local changes

# Demo Time!
