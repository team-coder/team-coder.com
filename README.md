# The Team Coder Blog

This repo contains the source code for the website at [team-coder.com](team-coder.com). It's built with [Jekyll](https://jekyllrb.com) and deployed via GitHub Pages.


## How to run the website locally

First, you have to install [Jekyll](https://jekyllrb.com/docs/).

Then, after checking out this GitHub repository, use the console to go to it's root directory. Type the following command to start the Jekyll server:

```bash
bundle exec jekyll serve
```

Once the server is running you can reach the website in your browser at [http://localhost:4000](http://localhost:4000).


## How to add a new blog post

You are very welcome to write a guest post. Here is what you have to do:

1. Create a new image directory for your post in the “images/posts/” directory. Use the same naming conventions as the other image directories ("YYYY-MM-DD-title-of-the-post").
2. Add a title image for your post to that directory (optional). Name it "title-image.jpg". It should have the resolution 845x384px. Also, add two images in lower resolutions. One with 440x200px (name it "title-image-440.jpg") and one with 220x100px (name it "title-image-220.jpg"). Different image sizes are used in different situations so if you want to have a title image you have to add all 3 image sizes.
3. Create a new markdown (.md) file in the “_posts/” directory. Again, use the same naming convention as the other markdown files (the file name is basically the same as the name of your image directory). The markdown file contains your actual blog post and some [Front Matter](https://jekyllrb.com/docs/front-matter/) at the top. It might look like this:

```markdown
---
layout: post
title:  "The SOLID Principles of Software Design by Examples"
author: "Robert Ecker"
date:   2015-12-19 12:00:00 +0200
categories: dev
image: ../images/posts/2015-12-19-the-solid-principles-of-software-design-by-examples/title-image.jpg
permalink: /solid-principles/
---

SOLID is an acronym for five principles that help software developers design maintainable and extendable classes. It stands for Single responsibility, Open-closed, Liskov substitution, Interface segregation and Dependency inversion...
```

4. Run the project locally (as described above).
5. Create a new pull request. As soon as it is merged into the *master* branch it will be published on [team-coder.com](team-coder.com) :tada:


## How to add a new category for blog posts

Categories are defined in the "_category" directory. If you want to add a new category, add a new markdown file with the name of your new category as it's file name. The content of your file might look like this:

```markdown
---
tag: dev
title: "Software Development"
permalink: "/category/dev"
---
```

- *tag* is what you will later add as a category in the Front Matter of your blog post.
- *title* is a more pretty version which is used on the category index page.
- *permalink* is the link for the category index page, which contains a list of all blog posts with that category. Stick with the conventions and use the "/category/" path!

If there are multiple blog post with the new category it might make sense to add it to the sidebar navigation.


## How to report a bug on the website

If you find a bug on [team-coder.com](team-coder.com) it would be awesome if you would let me know by creating an issue here on GitHub! For bonus points create a pull request which fixes the bug :grin:


## How to earn some extra karma points

If you like the Team Coder blog please tweet about it or share it in your preferred social network! If you like this GitHub repo and the fact that it's open source, feel free to give it a star :pray:
