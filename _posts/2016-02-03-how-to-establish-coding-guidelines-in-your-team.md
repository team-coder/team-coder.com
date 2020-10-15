---
layout: post
title:  "How to Establish Coding Guidelines in Your Team"
author: "Robert Ecker"
date:   2016-02-03 12:00:00 +0200
categories: dev
image: /images/posts/2016-02-03-how-to-establish-coding-guidelines-in-your-team/title-image.jpg
permalink: /establish-coding-guidelines/
description: In this article we tell you what is important if you want to establish coding guidelines in your team successfully.
---

Coding guidelines help software developing teams to write consistent code which is easy to read and understand for all team members. Establishing such guidelines can be problematic if it is done wrong but it will be very beneficial for the whole team if it is done the right way. In this article we tell you what is important if you want to establish coding guidelines in your team successfully.

**Note:** I have written this article together with [Stephan Huber](https://www.linkedin.com/in/stephan-huber-a11b2ba9), so he is the first guest author on *team-coder.com*. Here are his initial thoughts about the topic:

Defining the most suitable coding guidelines for a team seems to be hard. Usually, as an individual team member you have your own style how to write code and do not want to change this because every change slows you down in writing code. Imagine you would have to change your handwriting overnight. Crazy, isn’t it? However, that does not mean that there is no way to define and implement some coding guidelines for your team. It shows that you have to bring up the right arguments why coding guidelines are so important and try to support your team with additional proofing tools as guides.


## What are coding guidelines?

Often coding guidelines do not only describe the syntax of the code. They are not just about naming conventions or the position of curly brackets. They may also include definitions about the overall structure of code, like the class layout (e.g. member variables on top, then properties and constructor, public methods and so on) and well known design patterns like *Model-View-Controller*. We recommend that every coding guideline is based on existing guidelines for the specific programming language or framework. Examples are the [Cocoa Coding Guidelines](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html) by Apple or the [Design Guidelines for Developing Class Libraries](https://msdn.microsoft.com/en-us/library/ms229042(v=vs.100).aspx) by Microsoft. You don’t have to invent completely new guidelines. All you have to do is change the aspects that don’t match for your team.

Always remember: **Guidelines are guidelines, not rules!**


## The benefits of coding guidelines

Coding guidelines help us to write consistent code. It should not matter which developer in your team has written the code you are looking at. It should feel as if you had written the code yourself because it just conforms to your own style. Even if someone from outside your team has contributed something to your code base, e.g. in an open source project on GitHub, you want their code to fit perfectly into your internally written code base.

Guidelines also help us to always remember to write clean code. Don’t forget the future-you. When you have to change something in your code a year later you want to read and understand it quickly, which is more likely if you have followed a few clean-code guidelines. Team members with less experience will also learn to follow those guidelines from the beginning.

The coding guidelines are also a good starting point for new team members or external developers who support your team. They will understand your code structure more quickly and they will also feel more comfortable when they write new code because they know that their code will look the way you expect it.

Finally, the guidelines will have a positive effect on the costs for maintaining your software. Code will be understood faster if everybody has the same style writing it. Reading and understanding code consumes the biggest part of the time we spend on coding. If you can decrease the amount of time your team needs for reading and understanding, the whole team will be much more productive.


## How to agree on the right guidelines for your team

Coding guidelines are only useful if every team member takes them seriously. That’s why the whole team has to agree on the guidelines once they are finished. If one person works out some guidelines alone, chances are small that all team members will agree on them. But if everyone is involved in the process of writing down the guidelines it is much more likely that everybody will follow them.

I have established coding guidelines in several teams and I’ve found that the first thing you have to do is making sure that everybody in the team understands why coding guidelines are so beneficial. When everyone is convinced you can continue with the next step: Make and present a first draft to the team that contains the topics and some high level descriptions of the coding guidelines. I’ve created a list summarizing the points which seemed to be important to me and I shared the list with the whole team, asking them to give comments.

When all developers have had their time to think about my suggestions I called a meeting. If the team is small then everybody should attend. For huge teams it might be okay to invite only a few representatives. In the meeting we discussed all my points and added points which were important to other developers. We agreed on every point on the list by using the Consensus method which is described in this blog post about [Boosting the Quality of Team Decisions](https://team-coder.com/boosting-the-quality-of-team-decisions/). After agreeing on the guidelines the next step was to implement them.


## How to implement the coding guidelines

It is important that the guidelines, you have agreed on, are accessible for every developer in the team. New team members have to be introduced to the guidelines and of course every team mate can make proposals to improve the guidelines at any time.

You don’t have to change the whole code base of existing projects just to fit the guidelines. That would probably be too much work at once. Instead you should apply the new guidelines for every new line of code you write and for every part of the code you touch. Pull requests should not be merged if the code doesn’t conform to the guidelines.

In addition to documents or wikis you can use proofing tools like [ReSharper](https://www.jetbrains.com/resharper/) for C# or simple code formatters. They ensure that your coding guidelines are available right in your development environment. Such automation tools can help you and your team to learn guidelines and identify violations directly in your code during development. Of course some of the well known software development tools have already implemented some basic “code checkers” but often they do not really cover it all. We recommend to test out some proofing tools because they support your team in a direct way, unlike reading a lot of documents describing your coding guidelines. You can just learn everything on the fly. Some development environments (e.g. AppCode and other IDEs from JetBrains) already contain powerful proofing tools. Other tools are available as add-in for your existing development environment (e.g. ReSharper for MS Visual Studio and C# Development) or as a simple standalone script.

Have you ever tried to establish coding guidelines in your team? What have you learned? Please tell us about your experiences on Twitter!
