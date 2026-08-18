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


## Day 2 — GitHub Repository Management & Markdown

### Date

August 14, 2026

### Day 2 Objectives

* Learn the fundamentals of Markdown
* Understand the purpose and importance of `README.md`
* Learn how to organize a GitHub repository professionally
* Understand the purpose of `.gitignore`
* Learn why large bioinformatics data files should generally not be stored directly in Git repositories
* Understand GitHub Issues and their role in project management
* Distinguish between project documentation and source code
* Understand the importance of meaningful commit messages
* Continue practicing the local Git-to-GitHub workflow

---

## What I Learned

### 1. Markdown

Markdown is a lightweight markup language that allows plain-text files to be presented in a structured and professional format. Markdown files commonly use the `.md` extension and are automatically rendered by GitHub.

Markdown can be used to create:

* Headings and subheadings
* Bold and italic text
* Ordered and unordered lists
* Checklists
* Tables
* Hyperlinks
* Inline code
* Code blocks

Markdown is particularly useful for documenting computational and bioinformatics projects because technical explanations, commands, workflow information, and code examples can be presented clearly within the same document.

---

### 2. README Files

A `README.md` file provides an overview of a repository and helps readers quickly understand the purpose and organization of a project.

A professional README can contain sections such as:

* Project overview
* Objectives
* Dataset information
* Tools and software
* Installation instructions
* Workflow
* Usage instructions
* Results
* Repository structure
* Limitations
* Reproducibility information
* References

A well-written README is especially important when sharing projects with collaborators, researchers, reviewers, or potential employers because it allows someone unfamiliar with the project to understand its purpose without first examining every source-code file.

---

### 3. Repository Organization

Repository organization is important for maintaining projects in a clear, scalable, and professional manner.

Rather than storing all scripts, documentation, configuration files, results, and other materials in a single folder, files can be separated according to their purpose.

For example:

```text
bioinformatics-project/
├── README.md
├── src/
├── docs/
├── config/
├── tests/
└── results/
```

Organizing repositories in this manner improves readability and makes it easier for both the project developer and collaborators to locate and understand project components.

Repository organization becomes increasingly important as computational projects grow in size and complexity.

---

### 4. `.gitignore`

A `.gitignore` file tells Git which untracked files or file patterns should normally be excluded from version control.

For bioinformatics projects, this can be particularly useful because projects may generate large datasets, temporary files, intermediate results, environment files, or other materials that should not be committed to a repository.

Example:

```gitignore
# Large sequencing files
*.fastq
*.fastq.gz
*.bam
*.cram

# Python temporary files
__pycache__/
*.pyc

# Environment files
.env

# Temporary outputs
temp/
```

The `.gitignore` file therefore helps keep a repository focused on files that are appropriate for version control.

---

### 5. Large Bioinformatics Data Files

Large sequencing files such as FASTQ, BAM, and CRAM files should generally not be stored directly in ordinary Git repositories.

There are several reasons for this:

* Sequencing datasets can be extremely large.
* Large files can negatively affect repository size and performance.
* Git is primarily designed for versioning source code and text-based project files rather than very large genomic datasets.
* Some genomic datasets may contain sensitive, controlled, or clinical information that must not be publicly exposed.
* Public datasets can often be referenced through their database accession numbers rather than duplicated inside a GitHub repository.

For publicly available bioinformatics datasets, a reproducible project can instead document the source and accession and provide instructions or scripts for obtaining the data.

---

### 6. GitHub Issues

GitHub Issues are project-management tools that can be used to document and track work associated with a repository.

Issues can represent:

* Tasks
* Bugs
* Planned features
* Improvements
* Questions
* Documentation work

For example, a future NGS pipeline project might contain Issues such as:

```text
Add FastQC quality-control step
Implement BWA-MEM2 alignment
Add MultiQC reporting
Implement variant calling
Write validation documentation
```

An Issue organizes the work that needs to be completed; it does not itself modify the source code.

---

### 7. Documentation vs. Source Code

Documentation and source code serve different purposes within a repository.

**Documentation** explains the project to users, collaborators, and developers. It can describe the purpose of the project, installation procedures, workflow, inputs, outputs, results, limitations, and instructions for reproducing an analysis.

Examples include:

```text
README.md
docs/installation.md
docs/workflow.md
```

**Source code** contains the computational instructions that implement the functions of the project.

Examples include:

```text
analysis.py
main.nf
quality_control.R
```

Documentation may include small examples of code or commands, but its primary purpose is explanation rather than execution.

---

### 8. Meaningful Commit Messages

Commit messages should clearly describe the change being recorded.

For example:

Poor commit message:

```text
update
```

More informative commit message:

```text
Add bioinformatics file exclusions to .gitignore
```

Meaningful commit messages make repository history easier to understand and allow developers and collaborators to identify when particular changes were introduced.

For a bioinformatics workflow, useful commit messages could include:

```text
Add FastQC quality-control module
Add BWA alignment configuration
Update variant filtering thresholds
Add MultiQC report generation
Document pipeline validation procedure
```

The commit history can therefore provide a concise record of how a project developed over time.

---

## Git Workflow Reinforcement

I reinforced the Git workflow learned during Day 1:

```text
Edit or create file
        ↓
Save file
        ↓
git status
        ↓
git add <filename>
        ↓
Staging Area
        ↓
git commit -m "Meaningful description"
        ↓
Local Git Repository
        ↓
git push
        ↓
GitHub Remote Repository
```

For example, after modifying a tracked `README.md` file:

```bash
git status
git add README.md
git commit -m "Update project README documentation"
git push
```

---

## Markdown Syntax Practiced

### Headings

```markdown
# Main Heading
## Section
### Subsection
```

### Text Formatting

```markdown
**Bold text**

*Italic text*

`inline code`
```

### Bullet Lists

```markdown
- Git
- GitHub
- Docker
- Nextflow
```

### Numbered Lists

```markdown
1. Quality control
2. Alignment
3. Variant calling
4. Annotation
```

### Checklists

```markdown
- [x] Learn Git fundamentals
- [x] Create a local repository
- [x] Push repository to GitHub
- [x] Learn Markdown
- [ ] Learn branches
- [ ] Learn Pull Requests
```

### Tables

```markdown
| Tool | Purpose |
|---|---|
| Git | Version control |
| GitHub | Repository hosting and collaboration |
| Docker | Containerization |
| Nextflow | Workflow management |
```

### Code Blocks

A fenced code block can be used to document commands:

```bash
git status
git add README.md
git commit -m "Update documentation"
git push
```

---

## Commands Reinforced

The Git commands practiced or reinforced during Days 1 and 2 include:

```bash
git status
git add <filename>
git commit -m "Commit message"
git push
git log
git remote -v
```

---

## Day 2 Knowledge Check

By the end of Day 2, I was able to explain:

1. What Markdown is and why it is useful.
2. Why a `README.md` file is important.
3. How `.gitignore` controls which untracked files Git normally ignores.
4. Why large FASTQ, BAM, and similar genomic data files generally should not be stored directly in Git repositories.
5. How GitHub Issues can be used for project management.
6. The difference between documentation and source code.
7. Why professional repository organization is important.
8. Why meaningful commit messages improve project history.
9. How to update a locally modified file and push the committed change to GitHub.

---

## Key Takeaway

Day 2 expanded my understanding of GitHub beyond simply storing code. A professional repository should be structured, documented, maintainable, and understandable to other users.

For bioinformatics projects, GitHub can be used to maintain source code, workflow definitions, configuration files, documentation, tests, and other reproducibility-related materials, while large or sensitive datasets should be managed through appropriate external storage or controlled data resources.

Clear Markdown documentation, organized repository structures, appropriate `.gitignore` rules, meaningful commit messages, and GitHub Issues can collectively improve the maintainability and reproducibility of computational projects.

---

## Day 2 Status

**Completed**


### Key Takeaway

Git provides a structured way to track the development history of a project rather than simply storing copies of files. GitHub extends this workflow by providing an online environment where Git repositories can be stored, shared, reviewed, and collaboratively developed.

For bioinformatics, this approach can support reproducibility by maintaining a traceable history of changes to scripts, workflows, configuration files, and project documentation.


## Day 3 — Branches, Pull Requests, Merging & Collaboration

### Date

August 15, 2026

### Day 3 Objectives

* Understand the purpose of Git branches
* Learn how branches support safe and organized development
* Create and switch between branches using Git
* Understand how feature branches differ from the `main` branch
* Push a feature branch to GitHub
* Create my first Pull Request
* Review proposed changes before merging
* Merge a feature branch into `main`
* Synchronize changes between GitHub and the local Git repository
* Understand how branching workflows support collaborative bioinformatics development

---

## What I Learned

### 1. Branches

A branch is a separate line of development within the same Git repository.

Branches allow developers to work on new features, experiments, documentation, or fixes without immediately modifying the stable `main` branch.

For example:

```text
main
  │
  ●────●
        \
         ●────●  feature/readme
```

In this example, `feature/readme` can contain new work while `main` remains unchanged.

This makes branching especially useful for larger projects because development work can be completed and reviewed before being integrated into the main version of the repository.

---

### 2. Why Changes Are Not Always Made Directly on `main`

The `main` branch typically represents the primary or stable version of a project.

Making every experimental or unfinished change directly on `main` can introduce:

* Broken code
* Incomplete features
* Documentation errors
* Unintended changes
* Confusion between collaborators

A feature branch provides a safer workspace where changes can be developed independently.

For example:

```text
main
    ↓
Stable workflow

feature/add-multiqc
    ↓
New functionality under development
```

Once the work is completed and reviewed, it can be merged into `main`.

---

### 3. Creating and Switching Branches

I learned that the following command creates a new branch and immediately switches to it:

```bash
git switch -c feature/readme
```

The command can be interpreted as:

```text
git switch
     ↓
Switch branches

-c
     ↓
Create a new branch

feature/readme
     ↓
Name of the new branch
```

To switch back to an existing branch:

```bash
git switch main
```

---

### 4. Identifying the Current Branch

The command:

```bash
git branch
```

lists the available local branches.

For example:

```text
  main
* feature/readme
```

The `*` indicates the currently checked-out branch.

The branch is different from the working directory. The working directory remains the local project folder, while the checked-out branch determines which version of the repository I am currently working with.

---

### 5. Feature Branch Workflow

During the hands-on exercise, I created a feature branch for README development.

The general workflow was:

```text
main
  ↓
Create feature branch
  ↓
Make changes
  ↓
Stage changes
  ↓
Commit changes
  ↓
Push feature branch
  ↓
Create Pull Request
```

This allowed me to work on the README without directly modifying `main`.

---

### 6. Pushing a Feature Branch

After creating and committing changes on my feature branch, I pushed the branch to GitHub using:

```bash
git push -u origin feature/readme
```

This created a relationship between:

```text
Local branch:
feature/readme

Remote branch:
origin/feature/readme
```

The `-u` option establishes the upstream tracking relationship, allowing future pushes from the same branch to usually use:

```bash
git push
```

---

### 7. Pull Requests

A Pull Request is a GitHub feature used to propose that changes from one branch be reviewed and integrated into another branch.

A Pull Request does not automatically merge the changes. Instead, it creates a review point where the proposed changes can be examined before they are accepted.

The workflow is:

```text
Feature Branch
      ↓
Pull Request
      ↓
Review
      ↓
Approval
      ↓
Merge
```

I successfully created my first Pull Request on GitHub during this exercise.

---

### 8. Base and Compare Branches

When creating the Pull Request, GitHub displayed:

```text
base: main ← compare: feature/readme
```

This means that changes from:

```text
feature/readme
```

are being proposed for integration into:

```text
main
```

In this case:

```text
Source:
feature/readme

Destination:
main
```

---

### 9. Reviewing Files Changed

Before merging the Pull Request, I reviewed the **Files changed** section.

This step is important because it allows the developer or reviewer to inspect:

* Files that were modified
* Lines that were added
* Lines that were removed
* Unintended changes
* Accidental deletions
* Duplicate or unnecessary content

Reviewing changes before merging reduces the risk of introducing errors into the main branch.

This is an important component of professional code review.

---

### 10. Merging

Merging integrates the changes and development history from one branch into another branch.

For example:

```text
main
  ●────●
        \
         ●────●  feature/readme
```

After the branch is reviewed and merged:

```text
main
  ●────●──────●
        \     /
         ●───●
```

The work completed on the feature branch becomes part of `main`.

Merging is not simply combining two files. A branch may contain changes across multiple files, scripts, configurations, or documentation.

---

### 11. Local and Remote Synchronization

An important lesson from this exercise was that changes performed on GitHub are not automatically reflected in the local repository.

After merging the Pull Request on GitHub, I switched back to my local `main` branch using:

```bash
git switch main
```

I then retrieved the updated remote changes using:

```bash
git pull
```

The workflow was:

```text
GitHub main
     ↓
git pull
     ↓
Local main
```

This synchronized the local repository with the updated `main` branch on GitHub.

---

## Commands Practiced

During Day 3, I practiced the following Git commands:

```bash
git status
git branch
git switch -c feature/readme
git switch main
git add <filename>
git commit -m "Meaningful commit message"
git push -u origin feature/readme
git push
git pull
git log --oneline --all --graph
```

---

## Git Branching Workflow

The complete workflow practiced during Day 3 was:

```text
Local main
     ↓
Create feature branch
     ↓
git switch -c feature/readme
     ↓
Modify project files
     ↓
git status
     ↓
git add
     ↓
git commit
     ↓
git push
     ↓
Remote feature branch on GitHub
     ↓
Pull Request
     ↓
Review Files Changed
     ↓
Merge into main
     ↓
Remote main updated
     ↓
git switch main
     ↓
git pull
     ↓
Local main synchronized
```

---

## Application to Bioinformatics

Branching and Pull Requests are particularly useful in bioinformatics software and pipeline development.

For example, a bioinformatics pipeline might use separate branches for:

```text
feature/add-fastqc
feature/add-multiqc
feature/gatk-variant-calling
feature/vep-annotation
fix/reference-genome-path
docs/validation-procedure
```

Developers can test each feature independently before integrating it into the stable pipeline.

This approach can help prevent experimental changes from breaking a validated or working workflow.

For collaborative bioinformatics projects, Pull Requests also provide a structured mechanism for reviewing changes to:

* Python scripts
* R scripts
* Nextflow workflows
* Configuration files
* Quality-control modules
* Documentation
* Pipeline parameters

---

## Hands-On Activities Completed

* Created my first Git feature branch
* Switched between `main` and a feature branch
* Modified project documentation on the feature branch
* Staged and committed branch-specific changes
* Pushed a feature branch to GitHub
* Created my first GitHub Pull Request
* Reviewed the **Files changed** section
* Merged my first Pull Request into `main`
* Switched back to the local `main` branch
* Pulled the merged changes from GitHub
* Synchronized the local and remote repositories
* Practiced viewing branch and commit history

---

## Important Terminology Corrections

### Branch

A branch is not a separate repository.

It is a separate line of development within the same repository.

### `git switch`

`git switch` changes the currently checked-out branch, not the working directory.

### `*` in `git branch`

The `*` identifies the currently checked-out branch.

### Pull Request

A Pull Request proposes changes for review and potential integration. It does not itself automatically merge those changes.

### Merge

A merge integrates changes and development history from one branch into another.

---

## Key Takeaway

Day 3 introduced me to a professional Git and GitHub development workflow.

Instead of making every change directly on `main`, I learned how to develop work safely on feature branches, push those branches to GitHub, review changes through Pull Requests, merge approved changes, and synchronize the updated remote repository with my local repository.

The workflow I now understand is:

```text
Branch → Develop → Commit → Push → Pull Request → Review → Merge → Pull
```

This approach provides better organization, safer development, clearer project history, and improved collaboration.

For future bioinformatics projects, this workflow can help manage changes to pipelines, scripts, configuration files, documentation, and validation-related materials without immediately affecting the stable version of the project.

---

## Day 3 Status

**Completed**


## Day 4 — GitHub Issues, Linked Pull Requests and Merge Conflicts

### Topics Learned
- GitHub Issues for tracking bugs, features, documentation and project tasks
- Labels for organizing Issues
- Linking Issues with Pull Requests
- Using `Closes #<issue-number>`
- Issue → branch → commit → Pull Request → review → merge workflow
- Merge conflicts and why they occur
- Git conflict markers
- Manual conflict resolution
- Local vs remote branches
- Branch cleanup after successful merges
- Traceability in collaborative software development

### Hands-On Activities
- Created and labeled a GitHub Issue
- Created an Issue-specific feature branch
- Modified repository documentation
- Opened and reviewed a Pull Request
- Linked the Pull Request to an Issue
- Merged the Pull Request and closed the Issue
- Created a deliberate merge conflict
- Identified `HEAD` and incoming branch changes
- Manually resolved the conflict
- Staged and committed the resolution
- Deleted an obsolete merged branch

### Key Concepts
A merge conflict is not a Git failure. It occurs when Git cannot safely determine how competing changes should be combined and therefore requires human review.

A professional collaborative workflow can follow:

Issue → Feature Branch → Commits → Pull Request → Code Review → Merge

This workflow provides traceability, protects the stable `main` branch, and allows multiple developers to work independently.

### Day 4 Status
Completed
