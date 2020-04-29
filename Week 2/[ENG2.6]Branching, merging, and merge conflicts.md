# Branching, merging, and merge conflicts

This lesson introduces branching for team collaboration. This is how you work together on projects!

## Learning objectives

* TNTs will understand the basic of branching, merging, and resolving conflicts.
* TNTs will learn what is a merge conflict, what causes them, how to resolve and reduce.
* TNTs will be able to create and merge a branch locally and with GitHub.

## Time required and pace

Total time: 2 hours

* 60 minutes - pre-session: overview of branching and merging with git
* 20 minutes - explain: recap learning
* 30 minutes - explore: create and use a repo on GitHub
* 10 minutes - elaborate: review trouble spots

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

## Lesson details

### Recap learning (20 minutes)

1. Demo: cloning, branching, committing a repo from GitHib.
    1. We're going to review the basics of creating a branch and merging using GitHub.
    2. With Git Bash, clone the NameandFavFood repository.
    3. Create a new branch and check out to the branch.
    4. Open and edit the file in VS Code, adding name and favorite food.
    5. Commit the changes to the branch.
    6. Open a pull request to merge to master.
    7. In VS Code look at the pull request and complete the pull request.
    8. From master, make a change in GitHub added a fictitious name and food.
    9. From VS Code on the branch, make a change adding a different change

2. Best practices to resolve and reduce merge conflicts
    1. Git attempts to resolve differences in code. Merge conflicts occur when Git is unable to resolve the differences. This occurs when there are changes made to the same part of the same file on two different branches.
    2. Before attempting to merge, make sure any work in progress is either committed or merged. If you need to `git merge --abort` this will prevent you from loosing changes.
    3. Take a minute (or several) to understand the conflict. This will help you pick a solution to resolve the conflict.
    4. Decide what code should be included in master after the merge.
    6. Fetch from master and pull intro your branch frequently to stay in sync.

### Try it: clone repo, make branch, merge changes (30 minutes)

1. Spend the rest of time practicing and exploring Git.
2. Try - Adding your name and alias
     * Clone TNT repository 
     * Create a branch and add your name and alias to the txt file
     * Save, stage, and commit your change
     * Checkout to master and merge branch into master
     * Pull changes
     * Push changes
     * Look at the changes in GitHub, check out the branches and commits
     * Look at the changes in SourceTree, check out the branches and commits
     * Look at the source control tab in VS Code, check out the file diffs
3. By the end of the lesson you should have a repository that shows a history of changes, branches, merges.
4. If you get stuck or discover something cool, share it with a neighbor.

## Stretch

* Checkout learning modules on GitHub: [Managing merge conflicts](https://lab.github.com/githubtraining/managing-merge-conflicts) or [Ramp up on Git and GitHub](https://lab.github.com/githubtraining/paths/ramp-up-on-git-and-github)
