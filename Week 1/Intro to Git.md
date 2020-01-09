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
* [Automated Version Control with Git](http://swcarpentry.github.io/git-novice/01-basics/)
* [Ada Developers Academy Intro to Git](https://github.com/Ada-Developers-Academy/textbook-curriculum/blob/master/00-programming-fundamentals/git-intro-to-git.md)
* [Udacity Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)
* [How to Teach Git](https://recompilermag.com/issues/issue-1/how-to-teach-git/)

Pre-reqs
* [Install VS Code](https://code.visualstudio.com/)
* [Install Git](https://git-scm.com/downloads)
* [Install SourceTree](https://www.sourcetreeapp.com/), BitBucket account also required
   * Don't install Mercurial

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

4. **Demo** - local work flow in VS Code
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
   * `git commit` to commit change

5. NTs create local workflow

6. **Demo** - Sourcetree 
Instructor demos Sourcetree by adding local repository and looking at history. 
   * Sourcetree is an app for interacting with Git repositories. It does a good job visualizing what's going on.
   * You can make changes to repos with both the command line in VS Code and Sourcetree, there's some overlap in functionality. Try both and find what works best.
   * Open / add local repo. Look at commits.
   * Make change and commit with Soucretree.
   * *Talk about staged vs unstaged commits?*

7. NTs look at repo in SourceTree, make change and commit. 

6. **Demo** - remote repository in VS Code with GitHub
Instructor demos pushing repository to GitHub and cloning a repository from GitHub.

7. Review - 

8. Clone?


## Stretch
[Links and other projects for further learning and exploration]

## Bonus
[xkcd](https://xkcd.com/1597/)