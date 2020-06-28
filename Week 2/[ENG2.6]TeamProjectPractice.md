# Team Project Practice

With this project NTs review a spec and break down the engineering work. The teams then merge initial changes for the project into the same repo and resolve and resolve any merge issues. **The goal is not to complete the prototype of the app rather gain experience breaking down the work, coding together, and resolving conflicts.**

## Learning objectives

* TNTs will understand how to break down work.
* TNTs will understand how to scope work.
* TNTs will practice merging and resolving merge conflicts.

## Time required and pace

Total time: 3 hours, 45 instruction, remaining work time

* 20 minutes - explain: introduce the spec, scoping, and breaking down work
* 40 minutes - explore: break down the engineering work and review with coaches, create and check-in first changes, resolve merge issues
* post-session: evaluate: NTs finish initial changes and resolve merge issues

## Background / review

None

## Lesson details

### Introduce spec, scoping, and breaking down work (20 min)

1. For this project you will be beaking down the work in the sample spec.  A spec, short for specification, is a description of the app and it's functionality. It defines what is being built while capturing the essentials of why and how it's being built.

2. There are two steps to the project:
    * Breakdown the engineering work.
    * Build the initial screens for the project, associated with the P0, most important work items, merge them in the same repo, and connect the navigation across the screens.
   
When you're done, you'll have the shell of the shell of the app that navigates between the major pages and some place holder controls to represent the functionality. It'll feel very much like a high-fidelity prototype. Today we'll start by looking the spec and breaking down the work. 
    
    Consult with and get feedback from your coaches before you start building the screens.

### Breakdown engineering work

Find the sample spec - [YourShare](https://github.com/tnt-summer-academy/Curriculum/blob/main/Reference/Sample%20spec%20-%20YourShare.md) in the Reference folder.

1. Create a new GitHub repository for your team and put a copy of the spec in your repo.
2. Break down the engineering work; consider what are the pieces it will take to build the user story or functionality.
   For the prototype purposes, consider what you can show in the UI that would later be back by real integration with other API's or services. For example, it might be out of scope for the prototype to introduce authentication flows. Instead use text boxes to mimic a sign-in experience.
3. After breaking down the work, assign the engineering work items to individuals.
   Make sure everyone has a significant contribution to building the app. A good starting place is to have people write down which pieces they'd like to work on then compare. Consider your strengths and the strengths of your team.
   - Remember that today you'll only be working on the P0 tasks.  You should break down all the tasks but be aware that today you're only going to be working on P0 (so make sure that everyone has something to work on today)
4. After you've broken down the work, review with your coaches.
   Once you have sign-off from your engineering coach you can start building.

### Code, branch, merge and resolve conflicts

Here are some tips getting stared on the team development of YourShare:

1. One person create a new, empty repository on GitHub and put the spec into it (this steps was already mentioned, above)
2. That one person clone the repo locally.
   - Make sure that you [rename your 'master' branch to 'main'](https://www.hanselman.com/blog/EasilyRenameYourGitDefaultBranchFromMasterToMain.aspx)
3. That one person start a new app with Create React App in the *main* branch, and then push that back to GitHub
4. Everyone clone the repository locally.
5. **Everyone creates a new branch for their user story.**
6. Work on your user story, commit frequently, push, merge back into main in functional chunks. Fetch from *main* frequently and merge into your branch.
7. When you hit a merge conflict, debug it together.
8. Once you have the basic flow of the app done and can move between the features, you're done! Make the final merges.
9. In the real world before moving to the next user story you would implement the full functionality described in the spec for the user story. We're stopping here for time.
