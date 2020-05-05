# Branching, merging, and merge conflicts

This lesson introduces branching for team collaboration. This is how you work together on projects!

## Learning objectives

* TNTs will understand the basic of branching, merging, and resolving conflicts.
* TNTs will learn what is a merge conflict, what causes them, how to resolve and reduce.
* TNTs will be able to create and merge a branch locally and with GitHub.

## Time required and pace

Total time: 2 hours

* 60 minutes - pre-session: overview of branching and merging with git
* 20 minutes - explain: recap learning and introduce Source Tree
* 30 minutes - explore: create and use a repo on GitHub
* 10 minutes - elaborate: regroup and review

## Pre-session (60 minutes)

### Overview on Git and working with branches

Watch this video [GIT: working with branches](https://www.youtube.com/watch?v=JTE2Fn_sCZs)

* Why branches?
* Creating a branch
* Working from a branch

### Overview of Git merge

Watch this video [GIT: merging and workflow](https://www.youtube.com/watch?v=0iuqXh0oojo)

* Why merging?
* Overview of branches in real world development

### Collaborate with Git module

Complete this learning module - [Edit code through branching and merging in Git](https://docs.microsoft.com/en-us/learn/modules/branch-merge-git/)
Use the sandbox for this exercise to preserve your local git configuration.

* Create branches with git
* Merge branches with git

## Session set up

* GitHub - create repository in group from NameandFavFood demo in Samples
* Source Tree installed and ready to go

## Lesson details

### Recap learning (30 minutes)

Here's how the team development process is applied with GitHub: [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/).

1. Demo: cloning, branching, committing a repo from GitHib.
    1. We're going to review the basics of creating a branch and merging using GitHub.
    2. With Git Bash, clone the NameandFavFood repository.
    3. Create a new branch and check out to the branch.
    4. Open and edit the file in VS Code, adding name and favorite food.
    5. Commit the changes to the branch.
    6. Open a pull request to merge to master.
    7. In VS Code look at the pull request and complete the pull request and merge.

2. Demo: show a merge conflict
    8. From master, make a change in GitHub added a fictitious name and food.
    9. From VS Code on the branch, make a change adding a different change.

3. Best practices to resolve and reduce merge conflicts
    1. Git attempts to resolve differences in code. Merge conflicts occur when Git is unable to resolve the differences. This occurs when there are changes made to the same part of the same file on two different branches.
    2. Before attempting to merge, make sure any work in progress is either committed or merged. If you need to `git merge --abort` this will prevent you from losing changes.
    3. Take a minute (or several) to understand the conflict. This will help you pick a solution to resolve the conflict.
    4. Decide what code should be included in master after the merge. Make the changes to resolve the conflict.
    5. Fetch from master and pull into your branch frequently to stay in sync.
    6. Plan the work. Breakdown who is working on what and what may conflict.

4. Using Source Tree
    1. Source Tree is a tool that shows repository history and actions visually.
    2. It has quick commands to branch and merge.  
    3. **To-DO: add source tree demo**

### Try it: add name and favorite food to the list (20 minutes)

1. Together we're going to create a whole bunch of merge conflicts.
2. Clone the NameandFavFood repository.
3. Using Source Tree create a branch named "firstnameLastInitial", for example "MichaelS".
4. Make a change adding your name, favorite food to the list. "Michael, soft pretzels".
5. Commit the change to your branch.
6. Make a pull request to push the changes.
7. Merge the branch and resolve the merge conflicts.
    * Be mindful not to delete other people's response.
    * You may have to deal with merge conflicts more than once through this process.
8. Delete your branch when you're done.

### Regroup and review (10 minutes)

1. Take a look at the repository commit history, look at all the changes!
2. At branches or pull requests outstanding?
3. Poll the room - what made this difficult? What helped?

## Stretch

* Checkout learning modules on GitHub: [Managing merge conflicts](https://lab.github.com/githubtraining/managing-merge-conflicts) or [Ramp up on Git and GitHub](https://lab.github.com/githubtraining/paths/ramp-up-on-git-and-github)

* Interactive online tutorial for practicing Git Branching: [Learn Git Branching](https://learngitbranching.js.org/)