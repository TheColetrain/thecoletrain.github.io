---
title:  Jekyll
Date: 2025-3-14
Categories:  Jekyll Chirpy
Tags: Jekyll Chirpy Static Site Generator
---


# THE JEKYLL PROJECT

I wanted to make a website with my resume and to highlight some fun projects I have done.  TechnoTim is one of my favorite YouTubers and he has a great discord.  So naturally, I wanted to do what he does.

I would advise to follow his guide and his notes, but then I will try and add some more notes, if you get stuck.


<iframe width="560" height="315" src="https://www.youtube.com/embed/F8iOU1ci19Q?si=QMUPZVlZZ_0uDWLG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


Here are his notes [Meet Jekyll - The Static Site Generator](https://technotim.live/posts/jekyll-docs-site/)

Here are Jekyll Install notes [Jekyll - Installation](https://jekyllrb.com/docs/installation/)

Here are Chirpy Notes  [Chirpy - Getting Started](https://chirpy.cotes.page/posts/getting-started/)


 - <h1>1 </h1> The First issue I had, and once you know, then you know, was to get the local site up.  I was running it on a VM on Proxmox.  I tried using the VM IP + Port *192.168.10.55:4000*  and I tried localhost:4000, but what would have made my life easy was just doing **`http://127.0.0.1:4000`**

 - <h1>2 </h1> How I actually got it to work in the first place is with VS Code. -  Half way down the page in blue. 
 >If you are using Dev Containers, you must run that command in the VS Code Terminal.`<  
 [Chirpy Getting started] (https://chirpy.cotes.page/posts/getting-started/)
 
 - <h1> 3 </h1> Also, you can add this to the top of your `_config.yml`
 ```yml
 # Server settings
 host: 192.168.1.55
 port: 4314
 ```

<h2> Here is a quote for you. <h3>
"Once you know what you are doing, it is really easy.  When you do NOT know what you are doing, it is really hard."
<br>
<br>
<br>


Site Structure
=============
Once you get it up and running, I guess all these Tech guys just know things intuitively.  But I dod not.  I did not know what the header meant, what all the codes were.

  ***`_site` Directory***:  This is the output directory where Jekyll generates the static site. You **do not** put your new files here directly. Instead, Jekyll automatically builds your site into the `_site` folder when you run `jekyll build`. It contains the final, generated HTML files, along with any other assets that Jekyll processes.

***`_tabs` Directory***: This is used for Jekyll's "Tabs" plugin that Chirpy uses. The `_tabs` directory typically contains markdown files or other content that is used to populate or generate content dynamically on your site (for example, tabs for navigating content).  If you make a new file under `_tabs'  Your are making a new page on the website.  The headers of those pages have numbers, if you want to change the order.

***For a new post***: Put the markdown file under `_posts/` with the correct filename format (`YEAR-MONTH-DAY-title.md`).  And it will "shoot over" to the `_site/posts` folder.

> ### To summarize:
>
> - You ***don’t*** manually put new files in `_site`.
> - New content like posts goes in `_posts`.
> - Static files or content like tabs might go in `_tabs`


=========================================

## PUSH TO GITHUB
`git status` Should show nothing at first<br> 
`git add .`    dont forget the period <br> 
`git status` will show green now. <br> 
`git commit -m "updated main" `  you can change the coment <br> 
`git push`  <br> 


 