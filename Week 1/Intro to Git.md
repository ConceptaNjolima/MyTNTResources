# Intro to Git
This lesson introduces the fundamentals of the Git workflow, backtracking, and collaborating.

## Learning objectives
* TNTs will understand what is source control and why we need it.
* TNTs will learn how their previous code or doc collaboration experience to aspects source control.
* TNTs will be able to work with a local and remote repository using Git.

## Time required and pace
Total time: 1.5 hour
* 10 minutes - engage: opening activity
* 20 minutes - explain
* 30 minutes - explore: specific activity
* 15 minutes - elaborate: review trouble spots
* 15 minutes - evaluate: specific activity to demonstrate understanding

## Background / review
* [Ramp up on Git and GitHub](https://lab.github.com/githubtraining/paths/ramp-up-on-git-and-github)
* [Automated Version Control with Git](http://swcarpentry.github.io/git-novice/01-basics/)
* [Ada Developers Academy Intro to Git](https://github.com/Ada-Developers-Academy/textbook-curriculum/blob/master/00-programming-fundamentals/git-intro-to-git.md)
* [Udacity Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)
* [How to Teach Git](https://recompilermag.com/issues/issue-1/how-to-teach-git/)

Pre-reqs
* [Install VS Code](https://code.visualstudio.com/)
* [Install Git](https://git-scm.com/downloads)
* [Install SourceTree](https://www.sourcetreeapp.com/), BitBucket account also required, don't install Mercurial

## Lesson details
### Source control and You (10 min)
1. In groups have NTs discuss the following questions:
   * Have you ever worked on a code project or a document with other people? How did you share? Google doc? Emailing? GitHub?
   * When working with other people on code or project, what has gone wrong? Have you gotten versions of the document mixed up? Have you lost changes?

2. Groups come back together and share.

3. Wrap up and connect to source control.
   * Source control enables code collaboration
   * Makes large projects with 1,000s of people possible
   * Makes it easy to manage your own changes and work

### Intro to version control and Git
1. What is Git?
   * Git is a tool
   * Git allows you to add, edit, and break your code without fear. Git creates save points along the way so you can go back.
   * Git allows you to make changes to a file and store those changes back in a central repository (repo), file archive hosted locally or online, privately or publicly
   * Technically it's a "distributed version control system" (VCS)
   * Distributed: each person who has their own copy of the code and history
   * Version: like a document that's being written, code changes over time. Saving and committing creates a version of it. Another version is created when you add more and save again.
   * Control: Git is the system and processes that controls creating new versions. It also manages multiple people collaborating on those files.

2. Why Git?
   * There are other version control systems. Git is the most popular, and an industry standard.
   * It has some advantages over a centralized system, that has a single copy of the code: 
       * It's quick to take action on your own copy 
       * It works locally and offline 
       * It makes having multiple branches, parallel world of code, easier

3. What is GitHub and why GitHub? (Show and describe)
    * GitHub is were projects live. Individuals and organizations use GitHib.
    * Files for a project are stored in a repository (repo). Each repo has its own URL.
    * GitHub repos can be public and open to contributions from anyone - open source software (OSS).
    * GitHub repos can be can be private, with access restricted to a an individual, few people, or an organization.
    * GitHub is the largest community world wide community developers and widely used in the industry.

4. Git Gotchyas
   * Git can mean several things - the name of the source control technology, the functionality built into VS Code, the file formats and protocols that underlies the system.
   * It’s both powerful (because it’s open-ended), plentiful (b/c it’s open source), and sometimes hard to use (because it’s open-ended).
   * It takes practice, it's a learned skill, it's not intuitive - ask your coaches about their Git disasters, everyone has a story.

5. **Demo** - local work flow in VS Code
Instructor demos the basic local workflow and then NTs will follow on their own.
   * `git init` - command to create a new repo
     * Create a new directory, folder, or choose an existing one
   * Create a new file. By default the repo is empty.
     * Multiple ways to do this - click new file button in Explorer, `ctrl+n`, `File` -> `New File`.
     * Name file with extension of file type "hello_world.ts".
     * See "U", untracked, file hasn't yet been committed.
   * `git commit` - commend to commit changes
     * Add commit message to describe change
   * Make a code change and save `ctrl+s`
     * See "M", modified, file has been changed but not committed
     * See changes in the Source Control tab of the Explorer.
   * `git commit` - command commit change

6. NTs create local workflow
   * *Steps? What to name it*

7. **Demo** - Sourcetree 
Instructor demos Sourcetree by adding local repository and looking at history. 
   * Sourcetree is an app for interacting with Git repositories. It does a good job visualizing what's going on.
   * You can make changes to repos with both the command line in VS Code and Sourcetree, there's some overlap in functionality. Try both and find what works best.
   * Open / add local repo. Look at commits.
   * Make change and commit with Soucretree.
   * *Talk about staged vs unstaged commits?*

8. NTs look at repo in SourceTree, make change and commit.

9. **Demo** - remote repository in VS Code with GitHub Instructor demos migrating repository to GitHub.
   * Create a new repo in GitHub, *want to do it by building in TNT repo or in individual?*
   * Select "upload existing file". Choose files.
   * Need to clone repo to start working from GitHub rather than the local only copy.

10. **Demo** - cloning, branching, committing, a repo from GitHib.
     * Clone - Many projects start from an existing repo. This is a more coming flow than starting locally.
       * View "Clone or download" button in GitHub.
       * Open new VS Code window. `git clone` + GitHub URL and start working from remote repo.
       * *How does Sourcetree work with a repo you've cloned but not through Sourcetree? If it's cloned from VS Code can you still use source tree?*
     * Branch - Branching creates a separate world, thread, for you to work in. By default you're in the master branch. 
       * Typically most work is done in a different branch and then merged with master.
       * If four people are working on a project, each person has a branch. If you have two different features you're working on, you can can make a branch for each.
       * You can see the branch in the VS Code status bar and Sourcetree.
       * `git create branch` - command to create new branch
       * Give it a name and VS Code will automatically switch to it.
       * `git publish branch` - command to publish it to the VS Code repo.
       * `git checkout` - command lists all the branches and lets you switch between them. This can also be switched from the status bar.
       * You can also create a branch in Sourcetree by clicking "Branch" button.

11. NTs create a repo and upload files, then clone from repo and create a branch.

12. **Demo** - change, stage, commit, then push
     * The cycle is make a change, stage, commit, then push.
     * Stage allows you to to commit some of the changes. If you're still working on part, you can stage and commit just what's ready.
     * If you don't need to stage you can commit everything.
     * Save. `git stage` `git commit` `git push`. 
     * View changes in branch. Repeat as you work.
  
13. **Demo** - Merge 
     * Changes are merged from other branches back into master. master is treated at as the source of truth. 
     * `git checkout` to master. 
     * `git merge` and select the branch you'd like to merge from into master.

14. NTs make and push changes, then merge branch.

15. Fetch
     * Changes are fetched from master back into your local master branch. This is important to stay up to date with changes other people may be making.
     * `git checkout` to your local master branch and then `get fetch` to get the changes from the server.

16. Review - 
     * Next up: undoing, merge conflicts, pull requests

17. NTs create a new repo, branches, merges 

## Stretch
[Links and other projects for further learning and exploration]

## Bonus
[xkcd](https://xkcd.com/1597/)