# learn-git
"A Comprehensive Guide to Git: From Basic to Advanced Concepts"
## Definition
"Git is a distributed version control system (DVCS) that helps developers track changes in their code, collaborate with others, and manage code history. It allows multiple contributors to work on a project simultaneously while maintaining a complete history of revisions."
## Basic Concepts
* [Version Control System (VCS)](#version-control)
* [Git Basics](#git-basic)
* [Repositories](#repositories)
* [Commits](#commits)
* [Branches](#branches)
* [Working Directory](#working-dir)
* [Staging Area (Index)](#staging-area)
* [Remote Repositories](#remote-repo)
## Intermediate Concepts
* [Git Merge](#merge)
* [Git Rebase](#merge)
* [Merge vs. Rebase](#merge-rebase)
* [Conflict Resolution](#conflict-resolve)
* [Branch Management:](#branch-management)
* [Remote Operations](#remote-operation)
* [Git Tags](#git-tag)
* [Gitignore](#git-ignore)

## Advanced Concepts
* [Git Hooks](#git-hook)
* [Reflog](#)
* [Submodules](#submodule)
* [Git Workflows](#git-workflow)
* [Git Bisect](#git-bisect)
* [Interactive Rebase](#)

## Version Control
Version Control System (VCS), also known as Source Code Management (SCM) or Revision Control System, is a critical tool used in software development to manage changes to code and track the history of a project's development.
Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.

### **Git**

>Git is a distributed version control system (DVCS) that allows developers to track changes in their code, collaborate with others, and manage code history. It enables multiple contributors to work on a project simultaneously while maintaining a complete history of revisions. Git is known for its speed, branching and merging capabilities, and efficient handling of distributed workflows.

**Key Features**
* **Distributed:** Each developer has a complete copy of the repository, facilitating offline work and independent branching.
*  **Branching and Merging:** Git excels in creating, merging, and managing branches, which is crucial for parallel development.
* **Commit Flexibility:** Developers can commit changes locally before pushing them to the central repository.
* **Rich History Tracking:** Git stores the entire history of the repository, allowing detailed tracking of changes.

### **SVN (Subversion)**

>SVN, or Subversion, is a centralized version control system that helps developers manage and track changes in their codebase. It relies on a central repository where all code changes are committed. Developers check out code from the central repository, work on it locally, and commit changes back to the central repository.

**Key Features**
* **Centralized:** SVN uses a single central repository where all code changes are stored and accessed by developers.
* **Branching and Merging:** SVN supports branching and merging, but it is often considered less flexible and more challenging to manage than Git.
* **Commit Workflow:** Developers typically commit changes directly to the central repository.
History Tracking: SVN tracks changes on a file-by-file basis.

**Comparison:**
* **Distributed vs. Centralized:** Git is distributed, allowing each developer to have a full copy of the repository. SVN is centralized, relying on a single central repository. 
* **Branching and Merging:** Git excels in branching and merging, making it easy to create, merge, and manage branches. SVN supports branching and merging but is often considered less flexible.
* **Commit Flexibility:** Git allows for committing changes locally before pushing them to the central repository, providing more flexibility. SVN typically requires a central com
* **History Tracking:** Git tracks changes at a finer granularity, storing the entire history of the repository. SVN tracks changes file-by-file.
* **Community and Popularity:** Git is widely adopted and has a vast community of users. SVN is less popular in recent years but still has its place in some environments.

## Git Basic
### Repository (Repo)
* A Git repository is the central place where your project's files and their complete history are stored.

* It consists of three main components: the working directory, the staging area (index), and the local repository.

* The local repository is typically stored in a hidden ```.git``` directory at the root of your project.
```
#Creating a Git repository
mkdir my_project
cd my_project
git init
```
### Working Directory
* The working directory is your local file system, where you create, edit, and organize your project files.

* It's the place where you interact with your code, make changes, and see the current state of your project.
```
# Editing files in the working directory
nano myfile.txt
```
### Staging Area (Index)
* The staging area, also known as the index, is an intermediate step between your working directory and the local repository.

* It acts as a "staging area" where you can select which changes you want to include in your next commit.

* It allows you to review and prepare your changes before they become part of the project's history.
```
# Staging changes for commit
git add file1.txt file2.txt
```
### Local Repository:
* The local repository is where Git stores all the project's commits, branches, tags, and history on your local machine.

* It is the core of Git and maintains the complete history of your project.

* The local repository is usually located in a hidden ```.git``` directory within your project's root.
```
# Creating a commit in the local repository
git commit -m "Initial commit"
```
### Remote Repository
* A remote repository is a copy of your local repository hosted on a remote server, often on platforms like GitHub or GitLab.

* Remote repositories enable collaboration, allowing multiple developers to work on the same project and share their changes.

```
# Pushing changes to a remote repository
git push origin master
```
### Commits
* Commits are snapshots of your project at specific points in time. Each commit records a set of changes made to your files.
* Commits are identified by a unique SHA-1 hash and are organized sequentially, forming a timeline of your project's history.
```
# Creating a new commit
git commit -m "Added login feature"
```
### Commit Messages
* Each commit is accompanied by a commit message. A good commit message explains the purpose of the changes made in that commit.

* Descriptive commit messages help you and your team understand why a change was made and what it accomplishe
```
# Adding a descriptive commit message
git commit -m "Fixed bug in payment processing"
```
### Version History
* Git maintains a detailed history of all commits, allowing you to track the evolution of your codebase.

* You can view the commit history using commands like git log, which displays information such as commit messages, authors, and commit timestamps.
```
# Viewing the commit history
git log
```
### Branches
* Git allows you to work on multiple independent lines of development using branches.

* Branches are like separate paths where you can make changes without affecting the main project until you decide to merge your changes.
```
# Creating a new branch
git branch feature-branch
```

