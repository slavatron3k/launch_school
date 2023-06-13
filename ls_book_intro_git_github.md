# Introduction to Git and GitHub

## Getting Started

### Introduction

#### Source Control Management 
* **Source control management (SCM)** is the system by which teams of programmers can efficiently and simultaneously (via branching and merging) iterate on **codebases**
    * e.g. git, SVN, CVS, Azure DevOps
    * Keeps a historical ledger of files and manages SCM workflows to improve team coordination

#### Code Repositories
* Files are stored in a **repository** or **repo**
    * In **git**, a repo is simply a directory and files

#### What is Version Control?
* Version control helps to keep track of every change made to a codebase via the tracking of its contributors' actions
    * Helps to protect valuable source code
    * Allows for the rolling back of changes
    * Facilitates the development, testing, and tracking processes

#### What is Git?
* Popular, distributed, and open source SCM tool

#### Local vs. Remote
* Git is a **distributed version control system (DVCS)**
    * No main repository
    * Developers work from local repos and push commits to each other
        * In practice, most use a central repository, like GitHub
    * A **local repo** refers to one located on the local computer whereas a **remote repo** is located on another computer

## Working Locally

### Creating Local Repositories

#### git init
* GitHub currently uses `main` as the primary branch
    *  `master` was used previously
* **`git init`**
    * Initializes git repo in the present directory
    * Do not nest repos

#### .git Directory
* The .git directory contains the configuration and metadata to successfully use SCM
* Git store configuration data in three spots
    * `/etc/gitconfig` (system wide config for all users and their repos)
    * `~/.gitconfig` (user specific config)
    * `REPOSITORY/.git/config` (repo specific config)

#### .gitignore
* The `gitignore` file allows for the delegation of data that is not to be included in the repo
    * It is advisable to create one for every git repo

#### Private Repos
* GitHub allows for the creation of data sensitive, private repos

### Tracking Change

#### git status
* **`git status`** shows us our **working tree** and **staging area**
    * Will show the new files in the working tree that can be **committed** to the repo

#### Creating a commit
* A commit is a grouping a changes across a files or files
* **`git add`** **stages** files for a commit
* **`git commit`** submits the commit

#### git log
**`git log`** provides a history of commits for the repo
* Keep the idea of **commit hygiene** in mind when scrolling through the log
    * Each commit should contain a logical group of changes

### Branching

#### What is Branching?
* A **branch** is a copy of all the code in a codebase

#### Why Would I Want to Branch?
* Branching allows developers to manipulate the codebase without risk
    * Supports feature development and experimentation
* A branch is **forked** from another existing branch (generally main)
    * The changes made in the forked branch can be committed to the parent through a **merge**

#### Local vs. Remote
* Branches can exist locally and remotely
    * A local branch can be set to **`track`** a remote branch

## Remote Repositories

### Introduction
* **Remote repos** are located off of the local machine

### GitHub

#### Connecting to a GitHub Repo
* **`git remote add origin https://github.com/GITHUBUSERNAME/REPONAME.git`**

#### What Did We Just Do?
* **`git remote`** is used to work with remote repos
    * **`add origin`** links to the specified remote repo
        * **`origin`** is an **alias** that is used to interact with a remote repo at a local level

#### git push
* A local repo can **track** a remote branch
* The **upstream repo** is defined as the default remote repo that is being tracked
    * **`git push -u origin main`**

#### git pull
* When the upstream repo is ahead of our local repo, we can update our local repo with **`pull`**
    * First, **`git fetch`** will grab the commit data for the changes made
    * **`git diff`** can then be used to examine the differences between the current commit in the local and remote repos
        * `---` removed lines
        * `+++` added lines
    * **`git pull -ff only`** grabs and applies the changes found within the remote repo
        ** `ff` is the flag for the **fast forward merge** option
        `pull` combines fetch and merge into one command