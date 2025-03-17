---
title: "Obsidian to GitHub Sync"
description: How to sync Obsidian with GitHub (Using a YouTube guide)
date: 2025-03-16 15:03:00 CST
layout: post
categories: [homelab, notes]
tags: [obsidian, GitHub, git, sync, token]   # Tag names should always be lowercase
permalink: /obsidian/
pin: no
toc: true
---


# Goal - Sync Obsidian with GitHub
## Purpose
I want to sync my Obsidian notes with GitHub so I could back the data up and also learn about the process. Also, It can sync across devices.

## Outline of the steps
- Download Git on your computer if you have not
- Generate a GitHub Personal Access Token.
- Create the folder on GitHub
- Create the folder on your PC
- Clone the repository locally.

## Guide Used (My Revision of the Guide Below)
-I liked this guide for generating the token. However, the linked guide is ambiguous about the token’s duration, and the video doesn’t set an expiration. “Security is not convenient.” Your call. [Token guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) I revised this guide a bit to what is below

1. In the upper-right corner of any page on GitHub, click your profile photo, then select  Settings.
2. In the left sidebar, click **Developer settings**.
3. In the left sidebar, under **Personal access tokens** click **Tokens (classic)**.
4. Select **Generate new token**, then **click Generate new token (classic)**.
5. In the "Note" field, give your token a descriptive name.
6. Choose the expiration length
7. You only need to check **Repo**
8. Click **Generate token.**
9. Copy the new token to your clipboard and paste it in a `.txt` file or something. Or save in PW manager, but we will need it soon.

## Create a Repository on GitHub
- Click **Repositories**
- The Green **NEW** button
- Name it.
- **Important**  Check the little box that says "Add a README"

## Install Git on your PC if it is not there
- [Install Git](https://git-scm.com/downloads)

## Make a folder on your PC
- Use File Explorer (or your preferred method) to create a new folder.

## Install the `Git` Plugin in Obsidian
- Click the Cog icon in the bottom left
- Middle of the page **Community Plugins**
- Type `Git`
- Click **Install**.
- Click **Enable**  (Two clicks, dont forget.)

## Get that token formatting going
- I liked that quick `.txt.` doc, becasue I am not a typer, I cut and paste, and it is good to have it in front of you.
- We need to get the format of this `https://<PERSONAL_ACCESS_TOKEN>@GitHub.com/<USERNAME>/<REPO>.git`
- For example:  `https://xxxxxxxxxxxxxxxxx@GitHub.com/TheColetrain/Obsidian.git`

## Clone the Repo
- you should have your Obsidian open in the folder you want to be synced with GitHub
- Run the command (Ctrl + P): **Git:Clone an existing remote repo**
- Paste your formatted URL including token in the first blank
- I say, Leave the second field blank, and hit enter. *(Read the next part before continuing)*

- ### I pretty much did this whole write up becasue **I had trouble with this part.**
    - The videos and guides all seem to type something in to that second field, "Obsidian" in my case.  When I typed "Obsidian" in the 2nd blank, then I got a `Obsidian>Obsidian` subdirectory scenereo.

    - Full disclosure.  I dont know nuttin'.  But When I got that subdirectory scenereo, I could see it made some hidden files, `.Obsidian` and it was linked somehow.  Because it didnt like me changing it. Maybe deleting the hidden files would have worked, but I ended up deleting the repository, and the folder.  Then I made a repository `Obsidian1` and folder `Obsidian1.` And did what I said above.

## Hope this Helps.

#### Below is my preferred Video that I found

<iframe width="560" height="315" src="https://www.YouTube.com/embed/ImrLbomFYA0?si=RzsGefLMTvnhKgcI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

>
>
>
#### Here is another Guide.  The video below this link, is redundant, as it can also be found in the guide.

[The Easiest Way to Connect Your Obsidian Vault with Github](https://linked-blog-starter.vercel.app/connect-obsidian-vault-with-github)
>
>
>


<iframe width="560" height="315" src="https://www.youtube.com/embed/5YZz38U20ws?si=jfjUMYiMZw6HEmqy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
