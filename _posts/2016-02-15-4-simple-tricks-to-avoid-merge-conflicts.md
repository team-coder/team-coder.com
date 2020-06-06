---
layout: post
title:  "4 Simple Tricks to Avoid Merge Conflicts"
author: "Robert Ecker"
date:   2016-02-15 12:00:00 +0200
categories: dev
image: ../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/title-image.jpg
permalink: /avoid-merge-conflicts/
---

[Git](https://git-scm.com/) is a great tool if you have multiple developers working on the same code base. However, there is one thing which can be very annoying if your team uses Git: *Merge conflicts*! Two developers have changed the same part of the code and then Git doesn’t know what to do. Fortunately, there are a few tricks to avoid merge conflicts and this article will tell you how!

## Trick #1: Short-Living Branches

Many big merge conflicts are results of long-living branches. If you work in your own branch for several days, or even weeks, the risk is high that someone else changes parts of the code you have touched in another branch. That would lead to merge conflicts. On the other hand, if you have a short-living branch, meaning it is merged back into the trunk or master branch after a few hours, there will probably be no merge conflict. Even if there is a conflict, it can usually be resolved very quickly because there is much less code to think about.

The following figures both show a master branch (the line in the middle) and some kind of feature branches. The difference between those figures is that the first one contains many short-living branches while the second one has only two long-living feature branches. The merge commits in the first figure are always green because the short branches have not caused any merge conflicts. In the second figure we have a red dot at the end which represents a merge conflict that was caused by two of the many commits in the long-living branches.

![short-living branches](../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/short-living-branches.png)
![long-living branches](../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/long-living-branches.png)

## Trick #2: Small Modules

![documents](../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/documents.png){: .img-align-right}
The *Single Responsibility Principle* (which is part of the [SOLID principles of software design](https://team-coder.com/solid-principles/)) says that “*a class should have one, and only one, reason to change*“. If we take this approach serious, there should never be a situation in which two developers change the same code at the same time because that would mean they are working on the same task. You see, a modular architecture and small classes do not only help to increase the quality of the code design but also decrease the chance for merge conflicts.

## Trick #3: Strong Communication

![communication](../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/communication.png){: .img-align-left}
“Communication is the key” – We have heard this phrase so many times… and it’s true! If all your team mates know what you are working on and which parts of the code you are touching they will try not to change the same code at the same time. If another developer wants to change a part of the code base which you are working on then it would probably be a good idea to work together which leads me to the fourth trick…

## Trick #4: Mob Programming

![mob programming](../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/mob-programming.png){: .img-align-right}
This trick is the most powerful of all because it can eliminate merge conflicts completely! [Mob Programming](https://team-coder.com/mob-programming/) means that the whole team is working together on the same computer. That makes merge conflicts impossible because the whole mob is working on the same branch.

This is how branching would typically look like with Mob Programming:

![mob programming branch](../images/posts/2016-02-15-4-simple-tricks-to-avoid-merge-conflicts/mob-programming-branch.png)

Do you know more tricks to avoid merge conflicts? I would really like to know them so feel free to write a comment on Twitter!
