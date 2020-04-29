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

* GitHub - create repository from NameandFavFood demo in Samples

## Lesson details

### Recap learning (20 minutes)

1. Demo: cloning, branching, committing a repo from GitHib.

     * *Add steps for command line*
     * Clone - Many projects start from an existing repo. This is a more common flow than starting locally.
       * View "Clone or download" button in GitHub.
       * Open new VS Code window. `git clone` + GitHub URL and start working from remote repo.
       * *How does Sourcetree work with a repo you've cloned but not through Sourcetree? If it's cloned from VS Code can you still use source tree?*
     * Branch - Branching creates a separate world, thread, for you to work in. By default you're in the master branch. 
       * Typically most work is done in a different branch and then merged with master.
       * If four people are working on a project, each person has a branch. If you have two different features you're working on, you can make a branch for each.
       * You can see the branch in the VS Code status bar and Sourcetree.
       * `git branch <branch name>` - command to create new branch
       * Give it a name and VS Code will automatically switch to it.
       * `git publish branch` - command to publish it to the VS Code repo.
       * `git checkout` - command lists all the branches and lets you switch between them. This can also be switched from the status bar.
       * You can also create a branch in Sourcetree by clicking "Branch" button.

2. Best practices to resolve and reduce merge conflicts


15. Fetch
     * Changes are fetched from master back into your local master branch. This is important to stay up to date with changes other people may be making.
     * `git checkout` to your local master branch and then `git fetch` to get the changes from the server.

16. **Try it** - NTs make and push changes, then merge branch, fetch changes from master to another branch.

## Git free time - branch, commit, push, pull, merge (15 minutes)

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
