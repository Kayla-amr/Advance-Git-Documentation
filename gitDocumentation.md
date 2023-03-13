# Git Documentation

## Git Basics

### What is Git?
Git is a free and open-source distributed version management system that can handle small to big projects with ease. It monitors code changes and allows different individuals working on the same project to collaborate by letting them merge modifications into a single version. Git is a popular version control system for software development and other applications.

### Why use Git? What problem does it slove?
Git facilitates efficient and productive teamwork and makes managing and maintaining code easier. Several issues with software development and version control are resolved by using Git. For example:
Collaboration: Git allows multiple people to work on the same codebase simultaneously, making it easy to merge their changes into a single version.

Git keeps track of all code modifications, making it simple to go back to earlier iterations if necessary.

When numerous persons attempt to alter the same code simultaneously, conflicts can occur. Git assists in resolving these conflicts.

Git makes it simple to set up and maintain several branches for various features or experimental modifications, enabling developers to work separately without impacting the primary source.

Git makes it simple to recover from unintentional deletions or data loss by offering a backup of the complete codebase.

Git offers auditing, which makes it simple to inspect the whole history of all code changes. This feature enables developers to keep track of changes and comprehend how the code changed over time.

### What is the difference between Git and Github?
The difference between the two is that Git is a version control tool for keeping track of code changes, and GitHub is a website for hosting Git repositories.

## Git rebase

### What is Git rebase?
Git rebase is a Git command that lets you merge changes from one branch into another by reapplying a sequence of patches in a new order or on a different base. It is used to synchronize a feature branch with the main branch, to concatenate many commits into one, and to delete or rearrange commits. Rebase can produce a more organized and linear Git history.

### What are some advantages and disadvantages of Git rebase? (At least 2 of each)
Advantages:
Rebase enables you to combine many commits into a single one, as well as to delete or reorganize commits, which can result in a cleaner and more coherent Git history.
Rebase's straightforward and quick integration of changes from one branch into another makes it a helpful tool for synchronizing a feature branch with the main branch.
Disadvantages:
If a branch has previously been shared with others and the rebase modifications are pushed to the shared branch, it might result in the loss of work since rebase rewrites the history of Git.
Rebase can cause confusion in the Git history as it modifies the commit, making it challenging to follow the original commit and its modifications.

### When shouldn't you use Git rebase? Why?
Git rebase should not be used when working with shared branches. It modifies the Git history, which may result in lost work if the rebase modifications are applied to a shared branch that has already been shared with others. Complex Collaboration Workflows are also another thing to avoid. It will make it difficult to settle issues in complicated situations since it applies changes one at a time. The alternative for this would be to use Git merging  in these circumstances as opposed to Git rebase.

### Create a new repo and demonstrate your knowledge of the following items with screenshots:


![This is an image](https://i.postimg.cc/y8Rn3vN7/Screenshot-2023-02-07-at-12-03-11-PM.png)

![This is an image](https://i.postimg.cc/26kxJY75/Screenshot-2023-02-07-at-12-07-13-PM.png)


## Git reset, checkout, and revert

### What is Git reset?
Git reset is a command that returns a Git repository's state to a given commit. It gives  the ability to reject changes in the working directory, unstage changes from the index, and reset the branch pointer to a specific commit.

### What is the difference between hard, mixed and soft?
—hard restores the branch pointer to the given commit and discards modifications made to the working directory. The working tree's index and file contents are both reset to reflect the given commit. This operation is harmful and cannot be reversed.
—mixed option unstages modifications to the index. Git does not monitor the modifications made to the working directory, but they are still maintained.
—soft returns the branch reference to the given commit. Changes to the index and working directory are saved and staged. If  you wish to relocate the branch pointer to a different commit while keeping the modifications in the working directory intact, use this option.

### What is Git checkout?
In Git, the command "git checkout" is used to change branches or to bring back files from a working tree. Contents of a file in your working directory can be restored to the repository's version with this tool. The repository's condition at a certain commit can also be utilized to generate a new branch.

### What is Git revert?
A Git repository can be changed back with the command "git revert." In contrast to git reset, which removes commits, git revert reverses changes by adding a new commit that undoes the modifications made by one or more earlier commits.

### In what ways are these commands the same and what ways are they different?
They are comparable in that they both let you change a Git repository's state, but they work in different ways to do it.
Git reset deletes all modifications and commits from the working tree and changes the branch reference to the given commit.
Using the git checkout command, you can swap between branches and restore the working tree's file contents to their previous repository state.
In order to undo changes and preserve the history of the Git repository, git revert generates a new commit that rolls back the modifications made by one or more earlier commits.

### When would you use reset, checkout, or revert? Why?
When you wish to override changes made to the working directory and relocate the branch pointer to a certain commit, you use the git reset command.
When you wish to swap between branches or return the contents of the files in the working tree to the repository's state, you use git checkout.
Use git revert to roll back changes in a Git repository without erasing the project's history.

### Create a new repo and demonstrate your knowledge of the following items with screenshots:


![This is an image](https://i.postimg.cc/C1c4p2cs/Screenshot-2023-02-07-at-12-11-41-PM.png)

![This is an image](https://i.postimg.cc/W4P8GgDg/Screenshot-2023-02-07-at-12-16-22-PM.png)

![This is an image](https://i.postimg.cc/6QL0YqRS/Screenshot-2023-02-07-at-12-18-47-PM.png)

 ##Git submodules

### What are Git submodules?
The contents of one Git repository can be included in another Git repository using Git submodules.

### When would you use a submodule?
When you wish to utilize and manage a different repository within your primary repository, submodules can come in handy. It can assist you in managing your project's dependencies and ensuring that the library you rely on is maintained. 

### What are the advantages and disadvantages of Git submodules?
Advantages: 
Git submodules let you divide a large project into smaller, easier-to-manage chunks. This facilitates code maintenance and reuse across several projects.
You can have separate Git repositories for each component of your project. This allows one to individually version control each component and manage its dependencies.

Disadvantages: 
For developers who are unfamiliar, submodules can make a project more difficult. More processes and more complicated concepts may be involved in managing submodules than in managing a single repository.
Git processes can be slowed down by submodules, particularly when cloning or updating a repository with a lot of submodules.
The integration of submodules with other technologies, such as continuous integration systems, might be challenging.

