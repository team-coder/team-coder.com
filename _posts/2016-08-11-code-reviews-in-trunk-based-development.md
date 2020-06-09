---
layout: post
title:  "Code Reviews in Trunk Based Development"
author: "Robert Ecker"
date:   2016-08-11 12:00:00 +0200
categories: dev
image: /images/posts/2016-08-11-code-reviews-in-trunk-based-development/title-image.jpg
---

A few months ago I published a [blog post](https://team-coder.com/from-git-flow-to-trunk-based-development/) about my team’s transition from Git Flow to trunk based development. We have found a way to get our code into the master branch very quickly. At the same time we are always ready to release our master with confidence which is the basis for our continuous delivery pipeline. We have less merge conflicts and we are able to enable or disable features at any time.

One topic I didn’t cover with this previous blog post is how and when we review our code. Within the last months we have found a practice that works very well for us. In this blog post you will learn how we still use small branches and pull requests without losing the benefits of trunk based development.


## Different Ways to Review Code

A code review can be done in many different ways. My team uses GitHub, so a very common approach for our code reviews are pull requests. However, there are situations where pull requests are not necessary. For example, if a feature is implemented in pair programming or [mob programming](https://team-coder.com/mob-programming/) then the code is already reviewed while it is written. We decided that it doesn’t have to be reviewed again but of course, everybody may look at the commits later on in GitHub and add comments. As a rule of thumb we agreed that every line of code has to be approved by at least one other developer before it is pushed into our master branch.


## The Early Pull Request

### Pull Requests in Git Flow
When we used Git Flow it was obvious when to do the code review: As soon as a feature was finished, the developer created a pull request for the branch to be merged. At least one other developer had to review the code from that pull request. If no issues were found the pull request was merged, otherwise a discussion started and often a few more commits followed until everybody was happy with the solution. When everybody was happy the feature was finally merged into the develop branch. For every feature we had one pull request.

### Pull Requests in Trunk Based Development
In trunk based development it is different. Since we want to merge our commits into the master branch as quickly as possible, we cannot wait until the complete feature is finished. Unlike in the original trunk based development approach we still use feature branches but we have much less divergence from the master branch than in Git Flow. We create a pull request as soon as the first commit is pushed into the feature branch. Of course that requires that no commit breaks anything or causes tests to fail. Remember that unfinished features can always be disabled with feature toggles.

Now, with part of the new feature committed and the pull request created, another developer from the team can review it. In most cases that doesn’t happen immediately because the developers don’t want to interrupt their work every time a team member pushes a commit. Instead, the code reviews are done when another developer is open for it. Meanwhile, the pull request might grow by a few commits.

The code is not always reviewed immediately after the commit but in most cases it reaches the master branch much quicker than in Git Flow.


## The Code Review Column

Most agile teams use Backlog items, so called tickets, to define their features. Those tickets can be found on a board on a wall in the office or, like in our team, virtually on a web tool like Jira. We used to have five columns on our Jira board: “Planned”, “In Progress”, “Code Review”, “Manual Testing” and “Done”. Every ticket had to pass all of those columns until it was officially done. This workflow made sense with Git Flow but now something has changed. Part of the code is already reviewed before the feature is finished. But a ticket cannot be in both the progress and the code review column at the same time. It would be also very annoying to move the ticket between progress and code review after every commit. We found two possible solutions to solve that issue.

### Ticket Micro Management
One solution could be to make the tickets smaller. So small that they can be done in a single commit. Then the workflow would stay the same but with much more tickets. I cannot recommend this because it tends to end up in ticket micro management. It will just take too much time to write all those tickets. In our team the product owner is responsible for creating the tickets. Even if the effort is okay for her, it is unlikely that she knows all the implementation steps before the developers start working on the tasks.

### Goodbye Code Review Column
A much better solution than to start a ticket micro management is to say goodbye to the code review column. It is just an unnecessary part of the process. Like we should always try to delete unused code we should also try to get rid of processes that slow us down unnecessarily. We deleted the code review column. We review our code while we still develop it. In Jira that means every ticket is “In Progress” until it is finished, reviewed and merged into the trunk.


## Continuous Progress
Basically the way we review our code has not changed dramatically since we do trunk based development. When we do pair programming or mob programming it is like an instant code review. If something is implemented by a single developer we create a pull request on GitHub. But unlike we did it with Git Flow we now don’t wait with the pull request until the complete feature is finished. We create it as early as possible and get our code into the trunk before the entire feature is done. Always reviewing and merging our code in small iterating steps allowed us to delete our code review column on Jira. What we have achieved is a fluent transition between implementation and code review.

**The results are both happy developers and continuous, visible progress!**
