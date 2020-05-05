# Git undoing and backtracking

This lesson reiterates the basics for fixing with Git when something goes awry.

## Learning objectives

* TNTs will understand what go can wrong with Git.
* TNTs will learn strategies for fixing with Git.
* TNTs will practice strategies for resolving issues with git.

## Time required and pace

Total time: 50 minutes

* 15 minutes - engage: practice explaining git
* 20 minutes - explain: revisit tactics for backtracking and undoing with git
* 15 minutes - explore and elaborate: specific activity

## Pre-session

None

## Background / review

* Git Bash
* VS Code

## Lesson details

### Practice explaining Git (15 minutes)

Thinking through how Git works and explaining to others is a good way to cement Git understanding. Git is also a common tool and skill in the industry. Questions related to git may come up in an interview.

1. In your team, each person select one of the following questions to answer:
    * What is Git?
    * What are some advantages of using Git?
    * How can you create a repository in Git?
    * What is `git add` used for?
    * What is a commit message?

2. Write a two part answer. Part A, the answer to the question. Part B, an example that elaborates on the definition.
    * Question: What is the difference between Git and GitHub?
    * A: Git is a version control system that manages and tracks source code history. GitHub is a cloud-based hosting services for managing Git Repositories.
    * B: Git can be used with local repositories and other cloud hosting repositories like GitLab or BitBucket. The cloud hosting services like GitHub support Git and introduce more features that support team development life cycle, with a graphical user interface, control, and task-management tools.

3. Post your answer into your team and discuss.

### Revisit tactics for backtracking and undoing with git (20 minutes)

We'll cover three scenarios: amending a commit, recovering a deleted file, and reverting a commit.

1. Demo: Amending a commit
    1. If your wrote the wrong thing in the last commit message, use "--amend" to overwrite the message. `git commit --amend -m "new message"`
    2. If you have staged changes, they will be added to the previous commit as well. In most cases it's better to create a new commit then amend when it comes to code changes.

2. Demo: recovering a deleted file
    1. If a file is accidentally deleted from a repository it can be recovered with `git checkout`. Using a specific file name will pull the file back from the index into the working tree.
    2. Delete a file manually using Finder or File Explorer. Use the command `git checkout -- <file_name>` to bring it back.
    3. If a file is deleted and it gets recorded in the index, it cannot be restored with just `git checkout`. Instead a two step process is used to un-stage the file deletion from Git and then use `git checkout`.
    4. Delete a file using `git rm <file_name>` use `git reset Head <file_name>` to restore the file in the index and then `git checkout -- <file_name>`.
        * HEAD is a reference to the current / latest commit on the working branch
        * Anything before the latest commit is called the detached HEAD

3. Demo: reverting a commit
    1. Sometimes you just need to go back to a previous version. Refactoring some code didn't head the direction you thought. You accidentally deleted some code that you actually needed. The layout changed in a way you didn't predict and you want a fresh take at it. Don't worry, you've been committing your work in strong reasonable chunks.
    2. `git revert HEAD` makes a change that's exactly the oppositely of the last commit.
    3. `git reset --hard HEAD^` removes the most recent commit and history

### Practice backtracking and undoing (15 minutes)

In this activity complete the three scenarios, amending a commit, recovering a deleted file, and reverting a commit. Post on Teams if you're blocked or have a tip to share.

1. Make a new directory, add some sample files, and begin tracking with git.
2. Edit the files in VS Code. Make several (3-5) commits.
3. Amend your last commit.
4. Delete a file. Restore the file.
5. Make another commit.
6. Revert the commit.
