---
layout: post
title:  "Mob Programming"
author: "Robert Ecker"
date:   2015-10-20 12:00:00 +0200
categories: dev
image: ../images/posts/2015-10-20-mob-programming/title-image.jpg
---

Mob Programming is like [Pair Programming](http://www.extremeprogramming.org/rules/pair.html) but even more amazing! Instead of two people working together you have a whole team “working at the same time, in the same space, at the same computer, on the same thing” ([http://mobprogramming.org](http://mobprogramming.org/)).

In this article you will learn how Mob Programming can help your team to share knowledge, improve the team spirit and, by the way, develop great software!


## Prerequisites

To start a Mob Programming session the first thing you need is a mob. That means you need at least three people. If you had only two it would be Pair Programming.
The second thing you need is a room in which the mob can work undisturbed. In the room should be a projector or at least a big screen so everybody can read the code easily from his or her seat.
Prerequisite number three is a computer. It doesn’t matter whether you use the same computer for the whole session or all participants bring their own notebook. The important thing is that the team uses only one computer at a time.
Before the team starts the Mob Programming session it has to agree on one goal it wants to achieve. This is very important! Don’t forget this! Without a clear focus the session won’t be effective.


## The act of creating

There are different roles in Mob Programming. The one at the keyboard is called the *driver*. The others are the *navigators*. They tell the driver what to type. The driver role is passed on periodically, for example after every commit or after a fixed time frame like 15 minutes if all developers work on the same computer. That means that a navigator will take the seat at the keyboard and become the driver. All ideas of all participants must always be treated with respect. No one is superior to others, all are considered equal during the coding. There will be some people who talk more and some who talk less. That’s no problem, since characters are different. Just make sure that everyone is involved.

After the Mob Programming session is done I would recommend doing a short retrospective. There are many things that can be done slightly different and the best way to find out what you have to change the next time is by talking about it with the whole team.


## The benefits

Mob Programming can help your team in many ways. Here are the benefits I have seen in almost every Mob Programming session I have attended:

### Team spirit
Doing something together will increase the team spirit. Creating code together creates a collective code ownership and invalidates blaming individual persons for being responsible for bugs. Most developers have more fun when they work in a group than when they work alone.

### Collective code knowledge
Knowledge silos are always dangerous. We don’t want to be dependent on one person because that creates bottlenecks regularly and chaos if that person leaves the company or even if he or she is just on holiday. This threat is non-existing for software that is created with a group of multiple developers (in this regard the team is threat save ;-)). If everyone takes part in creating code, it is also easier for everyone to maintain this code in the future.

### Knowledge distribution
Every developer has a unique way of coding. Watching another developer writing code can be very interesting because you see all the small steps you wouldn’t see in a code review. You can learn about the process of building instead of just seeing the result. You may also learn about tools another developer uses or shortcuts you didn’t know before.

### Learning a new technology or practice
If you want to establish a new technology or practice, like test-driven development, in your team then Mob Programming is one of the quickest ways for the team to learn it.

### Instant code review
Since all participants are looking at the same screen it is like an instant code review, which is much more effective than doing it after the coding without such a deep context. There is no extra time needed for doing the code review afterwards. The chance that a bug will find it’s way into the code is much smaller if so many eyes are watching the screen!

### On-boarding of new team members
Mob Programming is perfect for introducing new team members to the way the team works. New members learn about the coding style and the strengths and weaknesses of all the participants and vice versa the team gets a better image of the new developer. Questions can be answered and discussed immediately.


## When should you do Mob Programming?
Even though it would be possible to do Mob Programming for every task, this would not work for most teams. Normally, developers need some time on their own so they can try out a few things or read some articles or documentations. Some tasks are so trivial that it doesn’t make sense to do them with the whole team. But the more complex or critical a problem is the better it is to solve it with more than one person. Also for the positive effect on the team spirit and for the many things you can learn from the others it is worth doing Mob Programming regularly. If your team is new to the topic it will be a good start to do it once or twice a week for half a day. Use the retrospectives to learn how often your team wants to do it!

**Do you have any experiences with Mob Programming? Please share them in the comments section below! :-)**