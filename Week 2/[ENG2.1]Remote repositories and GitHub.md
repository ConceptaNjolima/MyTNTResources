# Title

[Description - this template accounts for individual / pre-lesson work, reading, videos to introduce key concepts]

## Learning objectives

* TNTs will be able to...
* TNTs will understand...
* TNTs will learn...

## Time required and pace

Total time: 2 hours

* 45 minutes - pre-session: background learning, research, and investigations
* 10 minutes - engage: opening activity
* 10 minutes - explain: recap learning
* 30 minutes - explore: specific activity
* 10 minutes - elaborate: review trouble spots
* 15 minutes - evaluate: specific activity to demonstrate understanding

## Pre-session

[Pre-virtual session material for NTs to review]

## Session set up

[Resources for instructors to get set up on lesson]

## Lesson details

10. **Demo** - remote repository in VS Code with GitHub Instructor demos migrating repository to GitHub.

   * Create a new repo in GitHub, *want to do it by building in TNT repo or in individual?*
   * Select "upload existing file". Choose files.
   * Need to clone repo to start working from GitHub rather than the local only copy.

11. **Demo** - cloning, branching, committing a repo from GitHib.

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

12. **Try it** - NTs create a repo and upload files, then clone from repo and create a branch.
---

13. **Demo** - change, stage, commit, then push

     * *Add steps for command line* Show both in VS Code and command line
     * The cycle is make a change, stage, commit, then push.
     * Stage allows you to to commit some of the changes. If you're still working on part, you can stage and commit just what's ready.
     * If you don't need to stage you can commit everything.
     * Save. `git stage` `git commit` `git push`. 
     * View changes in branch. Repeat as you work.
  
14. **Demo** - Merge 

     * Changes are merged from other branches back into master. master is treated as the source of truth. 
     * `git checkout` to master. 
     * `git merge` and select the branch you'd like to merge from into master.
     * Merge conflicts occur when multiple developers edit the same content. At this point, Git is asking for human input to fix the conflicts.
       *  Make changes in master eg: README.md and commit changes.
       * `git checkout` to branch and make changes to the same line of the file that was edited in master with different text.
       * `git checkout` to master and `git merge` branch
       * Resolve conflicts in VS Code.

15. Fetch

     * Changes are fetched from master back into your local master branch. This is important to stay up to date with changes other people may be making.
     * `git checkout` to your local master branch and then `git fetch` to get the changes from the server.

16. **Try it** - NTs make and push changes, then merge branch, fetch changes from master to another branch.

---

## Review and Git best practices (15 min)

1. Room discussion - What worked? Where did you get stuck?
     * Address trouble areas

2. Git best practices
     * It takes practice
     * Keep commits light - it's good to save often and keep the change set small, it'll be easier to merge
     * Take a minute to review your changes before checking-in - more time will be spent on debugging, diff tools make it easier to quickly glance

3. Next up: undoing, merge conflicts, pull requests
     * The first super power of Git is branches, the second is being able to undo your changes.
     * There are a few different strategies for undoing and more to talk about in collaborative coding.

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

[Links and other projects for further learning and exploration]