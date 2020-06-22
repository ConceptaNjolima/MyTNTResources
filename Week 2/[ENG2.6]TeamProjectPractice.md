# Team Project Practice

With this project NTs review a spec and break down the engineering work. The teams then merge initial changes for the project into the same repo and resolve and resolve any merge issues. The goal is not to complete the prototype of the app rather gain experience breaking down the work, coding together, and practicing resolving conflicts.

## Learning objectives

* TNTs will understand how to break down work.
* TNTs will understand how to scope work.
* TNTs will practice merging and resolving merge conflicts.

## Time required and pace

Total time: 3 hours, 45 instruction, remaining work time

* 10 minutes - engage: revisit best practices for resolving merge conflicts
* 20 minutes - explain: introduce the spec, scoping, and breaking down work
* 1 hours - explore: during work time teams break down the engineering work and review with coaches, create and check-in first changes, resolve merge issues
* 1.5 hour - evaluate: NTs finish initial changes and resolve merge issues

## Background / review

None

## Lesson details

### Revisit best practices for resolving merge conflicts (10 min)

Checkout [ENG 2.6] Branching, merging, and merge conflicts for a refresher.

### Introduce spec, scoping, and breaking down work (20 min)

1. For this project NTs will be beak down the work in the sample spec, short for specification, is a description of the app and it's functionality. It defines what is being built, while capturing the essentials of why it's being built and how.

2. There are two steps to the project:
    * By breaking down the engineering work.
    * Build the initial screens for the project, associated with the P0, most important work items, merge them in the same repo, and connect the navigation across the screens.
    * When you're done, you'll have the shell of the shell of the app that navigates between the major pages and some place holder controls to represent the functionality. It'll feel very much like a high-fidelity prototype.

3. Today we'll start by looking the spec and breaking down the work. Consult and get feedback from your coaches before you start building the screens.

### Breakdown engineering work

Find the sample spec - [YourShare](https://github.com/tnt-summer-academy/Curriculum/blob/master/Reference/Sample%20spec%20-%20YourShare.md) in the Reference folder.

1. Create a new GitHub repository for your team and put a copy of the spec in your repo.
2. To break down the engineering work consider what are the pieces it will take to build the user story or functionality. For the prototype purposes, consider what you can show in the UI that would later be back by real integration with other API's or services. For example, it might be out of scope for the prototype to introduce authentication flows. Instead use text boxes to mimic a sign-in experience.
3. After breaking down the work, assign the engineering work items. Make sure everyone has a significant contribution to building the app. A good starting place is to have people write down which pieces they'd like to work on then compare. Consider your strengths and the strengths of your team.
4. After you've broken down the work, review with your coaches. Once you have sign-off from your engineering coach you can start building.

### Code, branch, merge and resolve conflicts

Here are some tips getting stared on the team development of YourShare:

1. Everyone clone the repository locally.
2. Everyone creates a new branch for their user story.
3. To get started, one persons starts a new app with Create React App in a branch, merges the branch.
4. Update your local master branch and merge it into your branch.
5. Work on your user story, commit frequently, push, merge back into master in functional chunks. Fetch from mast frequently and merge into your branch.
6. When you hit a merge conflict, debug to together.
7. Once you have the basics flow of the app in and can click between the screens, your done! Make the final merges.
8. In the real world before moving to the next user story you would implement the full functionality described in the spec for the user story. We're stopping here for time.
