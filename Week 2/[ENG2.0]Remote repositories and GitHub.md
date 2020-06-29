# Remote repositories and GitHub

This lesson introduces the core concepts for collaborating with Git and working with a remote repository.

## Learning objectives

* TNTs will understand the basic workflow for how multiple people work with git.
* TNTs will be able to clone a repository, make a pull request, push changes.
* TNTs will learn how to create and use repositories on GitHub.

## Time required and pace

Total time: 2.5 hour

* 55 minutes - [**Pre-session**](./https://github.com/tnt-summer-academy/Curriculum/wiki/%5BENG2.0%5D-Remote-Repositories-and-GitHub): background learning, research, and investigations
* 60 minutes - **Instructional Session**
    * 20 minutes - explain: recap learning
    * 30 minutes - explore: create and use a repo on GitHub
    * 10 minutes - elaborate: review trouble spots
* 30 minutes - [**Post-session**](./https://github.com/tnt-summer-academy/Curriculum/wiki/%5BENG2.0%5D-Remote-Repositories-and-GitHub): review, and investigations

## Pre-session (55 minutes)

Prepare for the session [here](../../../wiki/[ENG2.0]-Remote-Repositories-and-GitHub)

## Session Details
### Session set up

* GitHub - ready to make and clone a remote repository

## Lesson details

### Recap cloning and pull requests (30 min)

1. The learning module introduced the basics of cloning a repository and contributing to a repository using `git clone` and `git pull`. These are the building blocks for collaborating with Git and working with a remote repository.

<table style="border: none">
    <tr align="center">
        <td><img src="./remotes.png" alt="Clone, Pull and Push" width="80%"> </td>
    
</tr>
</table>


2. It's called a "pull request" because it's asking the main branch to pull in the changes.

3. Demo: Create a new repository in GitHub and clone using integrated terminal or Git Bash

We'll now walk through the process of cloning a repository from GitHub. We'll be creating a private repository in our own accounts.

    1. [Go to GitHub](https://github.com/) and create a new repository.
    2. Make an initial commit. Select create a Readme file as an initial commit

<table style="border: none">
    <tr>
        <td><img src="./CreateRemoteRepo.gif" alt="Create Remote Repo"> </td>
        <td><img src="./CloneURL.gif" alt="Clone URL"></td>
    </tr>
</table>


    3. With VS Code integrated terminal make a new directory `mkdir directory_name`
    4. Clone the remote repository to your local directory using `git clone` using the URL provided by GitHub.
    5. Show the folders and open the workspace in VS Code. you can just in the integrated terminal write `code .`

<table style="border: none">
    <tr align="center">
        <td><img src="./VSCodeRemoteClone.gif" width="75%" alt= "VS Code Clone"> </td> 
 </tr>
</table>


4. Demo: Clone from VS Code

    1. It's also possible to clone a repository from VS Code.
    2. Open the palette with Ctrl+Shit+P (Cmd+Shift+P for Mac OS).
    3. `Git: clone` prompts for a URL where you can paste from GitHub.

5. Demo: Make changes in VS Code and create a pull request

    1. With the folder open in VS code, add a new file and make changes to the existing file.
    2. In VS Code integrated terminal `^`\`, then  `git .add` to stage the files.
    3. `git commit` to create the commit. The changes are now committed locally.
    4. `git request-pull -p origin/main .` to create the pull request. `-p` means -p Include patch text in the output.
    6. `git remote` to know what are remote branch are available on your local.
    5. `git push origin master` to push the changes to the remote repo.

6. what is next?
    * Introduce Github workflow

<table style="border: none">
    <tr align="center">
        <td><img src="./GitHubWorkFlow.gif" width="75%" alt="GitHub work flow]"> 
    </td> 
 </tr>
</table>

    You can also read more about it from [here](https://guides.github.com/introduction/flow/)


7. Poll for questions

### Create and use a repo on GitHub (20 minutes)

The goal is to create a repo on GitHub, clone the repository, make changes in VS Code and push the changes back to GitHub.

1. Create a new private repository on GitHub. Make an initial commit adding a file from the website.
2. Clone the repository to your computer.
3. Open the folder in VS Code.
4. Add a new file in GitHub, edit the existing file.
5. Commit changes and make a pull request.
6. View the changes in GitHub.
7. Continue making changes in VS Code. Check out the `git diff`. Check out the log using `git log` ,`git log --oneline` or `git log --oneline --graph --decorate --all` to see the tracking of the commits.
8. Share a screenshot from GitHub of the commit history.

<table style="border: none">
    <tr align="center">
        <td><img src="./commitHistory.png" alt="commit History"> </td>
    </tr>
</table>


### Review trouble spots (10 minutes)

In your team's Team channel, discuss:

* What went well?
* What was difficult?