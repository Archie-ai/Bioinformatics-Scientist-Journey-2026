# Week 1 — Git & GitHub Learning Journal

## Day 1 — Git and GitHub Foundations

### Date

August 13, 2026

### Day 1 Objectives

* Understand what Git is
* Understand what GitHub is
* Understand the difference between Git and GitHub
* Learn basic Git and GitHub terminology
* Set up a professional GitHub profile
* Create my first professional repository
* Learn how repositories and README files are organized
* Understand the basic Git workflow
* Create and initialize my first local Git repository

### What I Learned

Today I learned the fundamental difference between Git and GitHub. Git is a version-control system that tracks changes to files and maintains project history, while GitHub is an online platform that hosts Git repositories and provides features for sharing, collaboration, and project management.

I learned that a repository serves as a project workspace containing files, documentation, and version history. A commit records a meaningful snapshot of selected project changes. I also learned that `push` transfers committed changes from a local Git repository to a remote repository such as GitHub, while `pull` retrieves and incorporates changes from the remote repository into the local repository. The `clone` operation can be used to create a local copy of an existing Git repository, including its version history.

I also learned the basic Git workflow:

**Working Directory → Staging Area → Commit → Local Git Repository → Push → GitHub**

During the hands-on exercise, I created a local project folder and initialized it as a Git repository using `git init`. I used `git status` to identify an untracked file and then staged the file using `git add`. After staging the file, I created my first commit using `git commit`.

I used `git log` to inspect the repository history and learned that every commit receives a unique commit hash. I also learned that `HEAD` identifies the currently checked-out position in the repository history and that the default branch can be renamed from `master` to `main`.

### Commands Practiced

* `git config`
* `git init`
* `git status`
* `git add`
* `git commit`
* `git log`
* `git branch -M main`

### Concepts Learned

* Git
* GitHub
* Repository
* Working directory
* Staging area
* Commit
* Commit hash
* `HEAD`
* Branch
* Push
* Pull
* Clone
* Local repository
* Remote repository

### Key Takeaway

Git provides a structured way to track the development history of a project rather than simply storing copies of files. GitHub extends this workflow by providing an online environment where Git repositories can be stored, shared, reviewed, and collaboratively developed.

For bioinformatics, this approach can support reproducibility by maintaining a traceable history of changes to scripts, workflows, configuration files, and project documentation.
