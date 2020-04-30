# Git undoing and backtracking

This lesson reiterates the basics for fixing with Git when something goes awry.

## Learning objectives

* TNTs will understand what go can wrong with Git.
* TNTs will learn strategies for fixing with Git.
* TNTs will practice strategies for resolving issues with git.

## Time required and pace

Total time: 45 minutes

* 10 minutes - engage: opening activity
* 20 minutes - explain
* 30 minutes - explore: specific activity
* 15 minutes - elaborate: review trouble spots
* 15 minutes - evaluate: specific Wactivity to demonstrate understanding

## Pre-session

None

## Background / review

[Resources for instructors, coaches, and students for ramp up or additional learning]

## Lesson details

### [opening activity] (10 minutes)

### Revisit tactics for backtracking and undoing with git (20 minutes)

We'll cover three scenarios: amending a commit, recovering a deleted file, and reverting a commit.

1. Demo: Amending a commit
    1. If your wrote the wrong thing in the last commit message, use "--amend" to overwrite the message. `git commit --amend -m "new message"`
    2. If you have staged changes, the will be added to the previous kit as well. In most cases it's better to create a new commit then amend when it comes to code changes.

2. Demo: recovering a deleted file
    1. If a file is accidentally delete from a repository it can be recovered with `git checkout`. Using a specific file name will pull the file back from the index into the working tree.
    2. Delete a file manually using Finder or File Explorer. Use the command `git checkout -- <file_name>` to bring it back.
    3. If a file is deleted and it's get recorded in the index, it cannot be restored with just `git checkout`. Instead a two step process is used to un-stage the file deletion from Git and then use `git checkout`.
    4. Delete a file using `git rm <file_name>` use `git reset Head <file_name>` to restore the file in the index and then `git checkout -- <file_name>`.
        * HEAD is a reference to the current / latest commit on the working branch
        * Anything before the latest commit is called the detached HEAD

3. Demo: reverting a commit
    1. Sometimes you just need to go back to a previous version. Refactoring some code didn't head the direction you thought. You accidentally deleted some code that you actually needed. The layout changed in a way you didn't predict and you want a fresh take at it. Don't worry, you've been committing your work in strong reasonable chunks.
    2. `git revert HEAD` makes a change that's exactly the oppositely of the last commit.
    3. `git reset --hard HEAD^` removes the most recent commit and history

## Stretch
[Links and other projects for further learning and exploration]
