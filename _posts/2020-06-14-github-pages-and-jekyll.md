---
layout: post
title:  "GitHub Pages and Jekyll"
author: "Robert Ecker"
date:   2020-06-14 08:00:00 +0200
categories: dev
image: /images/posts/2020-06-14-github-pages-and-jekyll/title-image.jpg
---

I have recently rebuilt this website with Jekyll and it is now deployed via GitHub Pages. In this article I will tell you why I did that and show you how I did it.

## About GitHub Pages and Jekyll
[GitHub Pages](https://pages.github.com) is a free web hosting service for static websites which are stored in Git repositories on GitHub. The website that is actually served is created by a generator, like [Jekyll](https://jekyllrb.com), which allows us to use templates for building up the HTML and SASS for assembling the CSS.


## Why I Use GitHub Pages and Jekyll
There seem to be endless ways and technologies for building a website. They range from setting up a Wordpress blog with almost no coding effort up to building a React frontend and a Node.js backend and setting up a MongoDB, all by yourself. Here are the reasons why I decided to use GitHub Pages and Jekyll for my blog:

### Markdown to HTML
When I write down my thoughts I always use Markdown. It's simple and doesn't require blown-up writing software like Microsoft Word. I can basically use any text editor for it. One thing that Jekyll does is it converts my markdown articles into HTML pages which is exactly what I need.

### History and Backups
I like the idea of having a complete history of all the changes I do on my website. In Git I can always go back in time and see what I wrote when. I can see what were my original words before editing a blog post. I can also see how my page was set up two years ago. All those things come built-in since with GitHub Pages everything is in a Git repository (unlike Wordpress for example). Also doing backups is easy because there are no databases. Just files and directories. Obviously, having a local version of the Git repository on my machine is already like a backup.

### Speed
GitHub Pages are hosted on GitHub servers and those are pretty fast. The average loading time of team-coder.com became much shorter when I moved it to GitHub.


## How I Set Up GitHub Pages and Jekyll

There are many different use cases for GitHub Pages and many different ways to set them up and build them. In this blog post I will not cover them all. Instead, I will let you know how I used GitHub Pages and Jekyll for building the blog that you are currently reading.

### Step 1: Setting Up a GitHub Project
For this blog, my first step was to create [this GitHub repository](https://github.com/team-coder/team-coder.com) in a GitHub organization which I created just for the Team Coder website. I could have also created the repository in my personal GitHub account but I prefer to have it independent from my personal account.

GitHub already offers a ready-to-use *.gitignore* file for Jekyll projects which I happily used when I created the repository.

### Step 2: Setting Up Jekyll
I found the most straight-forward instructions for installing Jekyll and initiating the Jekyll project on [Jekyll's official website](https://jekyllrb.com/docs/). I did exactly those steps.

Now, whenever I use my terminal to run this:

```bash
bundle exec jekyll serve
```

...my website becomes available at [http://localhost:4000](http://localhost:4000).

### Step 3: Coding
Step 3 is the most interesting part and I decided to not loose too many words about it :-P
To be honest, the project that Jekyll sets up initially is pretty self-explanatory. Again, the [Jekyll website](https://jekyllrb.com/docs/) perfectly explains all the details. If it is helpful for you, you are welcome to have a look at the [source code of team-coder.com](https://github.com/team-coder/team-coder.com).

### Step 4: Adding Content
I store all my blog posts as markdown files in the *_posts* directory. For all the images I want to use in those posts I created an extra directory in the root of my project and called it *images*. Among other images, like the Team Coder logo, it contains a directory called *posts* and that contains directories for all of my blog posts. That way I have all my images separated and assigned to their posts which seems to be the most clean structure to me.

**Note:** You can write HTML code in your markdown files as well. This can be helpful if you want to use structures that are not supported by Markdown, like tables with multiple rows in one cell. All you need is the `{::nomarkdown}` tag like this:

```markdown
|Name |Bullet Points                                   |
|-----|------------------------------------------------|
|Joe  |{::nomarkdown}<ul><li>bullet point</li></ul>{:/}|
```

### Step 5: Publishing the Website on github.io
Publishing the website on github.io is simple. There is a section called *GitHub Pages* in the *Settings / Options* menu of every repository on GitHub. Selecting the master branch as a source will publish the website and make it available on *https://TEAM-OR-USER-NAME.github.io/REPO-NAME*.

### Step 6: Using a Custom Domain
I don't want to have *https://team-coder.github.io/team-coder.com* as a domain for my blog. I want *https://team-coder.com*. Setting that up requires some configuration. The instructions on [this GitHub page](https://help.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site) helped me to get the job done. After changing the records at my DNS provider it took a couple of hours until my GitHub Page was available on [https://team-coder.com](https://team-coder.com).


## My Recommendation
Creating this website with Jekyll was a lot of fun. The flexibility is great, I did never reach the point where I couldn't implement something for technical reasons. Building the layout with templates and SASS was also a plesant experience. I love how I can easily push my new blog posts as Markdown files to Github and have them rendered as HTML pages. The whole thing feels very lightweight and it is also much faster than the old version of this website. For a static website like this I can absolutely recommend using GitHub Pages with Jekyll.
