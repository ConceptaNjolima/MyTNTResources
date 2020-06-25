# Git undoing and backtracking

This lesson reiterates the basics for fixing with Git when something goes awry.

## Learning objectives

* TNTs will understand what go can wrong with Git.
* TNTs will learn strategies for fixing with Git.
* TNTs will practice strategies for resolving issues with git.

## Time required and pace

Total time: 80 minutes

* 60 minutes - **Instructional Session**
    * 15 minutes - engage: practice explaining git
    * 20 minutes - explain: revisit tactics for backtracking and undoing with git
    * 15 minutes - explore and elaborate: specific activity
* 20 minutes - [**Post-session**](../wiki/[ENG1.5]-Git-undoing-and-backtracking): background learning, review, and investigations

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

### Revisit tactics for backtracking and undoing with git (30 minutes)

We'll cover three scenarios: amending a commit, recovering a deleted file, and reverting a commit.

1. **Demo: Amending a commit**
    1. If your wrote the wrong thing in the last commit message, use "--amend" to overwrite the message. `git commit --amend -m "new message"`
    2. If you have staged changes, they will be added to the previous commit as well. In most cases it's better to create a new commit then amend when it comes to code changes.

2. **Demo: recovering a deleted file**
    * <ins>*I deleted a file but didn’t commit:*</ins>
    You deleted a file, and immediately realized it was a mistake?  
    If a file is accidentally deleted from a repository it can be recovered with `git checkout`. Using a specific file name will pull the file back from the index into the working tree.

     ![recovering a deleted file](./[ENG1.5]recovering-a-deleted-file.png)

    * <ins>*I deleted a file and committed the deletion:*</ins>
    You made a commit deleting a file, but then realized you wanted to keep the file around after all? Do a reset to go back to the state before your commit (be careful: the "--hard" option means the command will discard changes to tracked files after the specified commit — you can also leave this option out in which case the file deletion will show up as an un-staged change along with any other changes you’ve made in your working tree. The file can then be restored as in the previous scenario):
    `$ git reset --hard HEAD~1`
    
    (Note: this presumes you haven’t already pushed your commit to a remote — this will be covered later next week.

    ![hard rest](./[ENG1.5]recovering-a-deleted-file-aftercommit.png)


    * *<ins>I committed the deletion and then I did more commits</ins>*
    If you deleted a file, committed, then continued work and did more commits, only to find that deleting the file was a mistake, Git still has you covered! To find the right commit, first check the history for the deleted file: `$ git log -- <filename>` 
    
        You can either work with the last commit that still had the file, or the commit that deleted the file. In the first case, just checkout the file from that commit: 
    `$ git checkout <commit hash> -- <filename>`
    
         In the second case, checkout the file from one commit before that:
         
    `$ git checkout <deletion commit hash>~1 -- <filename>`
         
    ![recovering a deleted file after new commit](./[ENG1.5]recover-deleted-after-newcommit.png)

    

3. **Demo: reverting a commit**
    
    Sometimes you just need to go back to a previous version. Refactoring some code didn't head the direction you thought. You accidentally deleted some code that you actually needed. The layout changed in a way you didn't predict and you want a fresh take at it. Don't worry, you've been committing your work in strong reasonable chunks.
    `git revert HEAD` makes a change that's exactly the oppositely of the last commit.

    ![git revert](./[ENG1.5]gitRevert.png)

    
***Note:*** `git revert HEAD` do the same as `git reset --hard HEAD^` but the second removes the most recent commit and history



## Recap for the common scenarios
 * I deleted a file but didn’t commit: use `$ git checkout HEAD <filename>`
 * I deleted a file and committed the deletion: use `git revert HEAD` or `$ git reset --hard HEAD~1` the second removes the most recent commit and history
 * I committed the deletion and then I did more commits**


### Practice backtracking and undoing (15 minutes)

In this activity complete the three scenarios, amending a commit, recovering a deleted file, and reverting a commit. Post on Teams if you're blocked or have a tip to share.

1. Make a new directory, add some sample files, and begin tracking with git.
2. Edit the files in VS Code. Make several (3-5) commits.
3. Amend your last commit.
4. Delete a file. Restore the file.
5. Make another commit.
6. Revert the commit.
7. Post the Git status to teams.

## Post-session

View the pre-session [here](../wiki/[ENG1.5]-Git-undoing-and-backtracking)