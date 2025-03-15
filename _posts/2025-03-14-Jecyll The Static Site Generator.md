---
title:  "Jekyll"
description: Making a website with Jekyll, Chirpy, and GitHub (Using a Youtube guide from Techno Tim)
date: 2025-03-14 10:03:00 CST
layout: post
categories:  [homelab, website]
tags: [jekyll, chirpy, github, docker, static site generator]   # Tag names should always be lowercase
permalink: /jekyll/
pin: true
toc: true
---

# The Jekyll Project - 

I wanted to create a website to showcase my resume and highlight some fun projects I've worked on. Techno Tim is one of my favorite YouTubers and tech enthusiasts, and he runs an awesome Discord. Naturally, I decided to follow his approach.

I recommend following his guide and notes; I'll add extra tips if you get stuck.


<iframe width="560" height="315" src="https://www.youtube.com/embed/F8iOU1ci19Q?si=QMUPZVlZZ_0uDWLG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


Here are his notes: [Meet Jekyll - The Static Site Generator](https://technotim.live/posts/jekyll-docs-site/)

Here are Jekyll installation notes: [Jekyll - Installation](https://jekyllrb.com/docs/installation/)

Here are Chirpy Notes:  [Chirpy - Getting Started](https://chirpy.cotes.page/posts/getting-started/)

# Viewing the site Internally

### 1. The first issue I encountered was getting the local site running. I was using a VM on Proxmox and tried accessing it:
  - Via the VM IP + Port (e.g. `192.168.10.55:4000`) *did not work* 
  - `localhost:4000` *did not work* 
  - In the short term, **`http://127.0.0.1:4000`** worked.  (But I did not think to try it for some time. I mistakingly thought localhost and 127.0.0.1 were the same, andthey are not. Seems easy now, but it took me a while before i realized. 😖 )  
  
### 2. I got it working using VS Code. 
    **If you are using Dev Containers, run the command in the VS Code Terminal.**
  [Chirpy Getting Started](https://chirpy.cotes.page/posts/getting-started/)
  (Look for the command highlighted in blue further down the page.)

### 3. Additionally, add the following to the top of your `_config.yml` (My favorite solution!):
 ```yml
 # Server settings
 host: 192.168.1.55
 port: 4314
 ```

## Here is a quote for you. 

"Once you know what you are doing, it is really easy.  When you do NOT know what you are doing, it is really hard." :laughing:


# Site Structure
Once you get it up and running, I guess all these Tech guys just know things intuitively.  But I did not.  I did not know what the header meant, what all the codes were.

**`_site` Directory**: This is the output directory where Jekyll generates the static site. **Do not** place new files here directly; instead, Jekyll builds your site into the `_site` folder.Producing the final HTML files and assets.

**`_tabs` Directory**: This is used for Jekyll's "Tabs" plugin that Chirpy uses. The `_tabs` directory typically contains markdown files or other content that is used to populate or generate content dynamically on your site (for example, tabs for navigating content).  If you make a new file under `_tabs'  Your are making a new page on the website.  The headers of those pages have numbers, if you want to change the order.

**For a new post**: Put the markdown file under `_posts/` with the correct filename format (`YEAR-MONTH-DAY-title.md`).  It will then be generated into the `_site/posts` folder.

# To summarize:
>
> - **Do Not** manually put new files in `_site`.
> - Place new posts in `_posts` With the date in the file name, properly formatted.
> - Static files or content like tabs might go in `_tabs`


# Tags and Categories
If you are using Chirpy, you need to figure out Tags and Categories. They will go in the heading syntax, in yaml format.  I will paste mine here without the lines "-" so you can see how it looks.

```yaml
title:  "Jekyll"
description: Making a website with Jekyll, Chirpy, and GitHub (Using a youtube guide from Techno Tim)
date: 2025-03-14 10:03:00 CST
layout: post
categories:  [homelab, website]
tags: [jekyll, chirpy, github, docker, static site generator]   # Tag names should always be lowercase
permalink: /jekyll/
pin: true
toc: true

```
Techno Tim talks in his video about this. Chekc that out. Says some important things, like lower case.  I am continuing that and explaining more about `tags` and `categories`  *What do they do?"* 😕 On the website on the left, there are sections labeled *tags* and *categories*  if you do this right, your tags and acetegories will show up there.
- `categories` are like a file folder sytem.  My main category in this instance is "homelab" and my subfolder is "website."  If I do other projects that are "homelab" they will go there, but if the second tag on the next project is them "kuberneties" then there will b a new sub folder there.  Check out my Categories section, if you want to see.
- `tags` are just that, and you can have a lot of them.  These are all going to be clustered on that page.
Lookat the above, and look at my site, hopefully this makes sense. On the home page they are the big words on the left. However, you are pretty close to the bottom of this page, and they are on the bottom of the page too! Hopefully I have helped explain, becasue I did not understand before.
  `tags` and `categories` are very much the same, but yet very different.  :smile:
  Here is the wiki on it, but it did not help me understand.
>>>>[Chirpy Wiki - Writing a New Post](https://chirpy.cotes.page/posts/write-a-new-post)



---
---

# Push To Github - Get it online, in the real world!
- `git status` Should show nothing at first, but could show pending changes.
- `git add .`    (Don't forget the period)
- `git status` will show green now.
- `git commit -m "updated main" `  (Change the comment to what is appropriate.)
- `git push`


 