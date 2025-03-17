---
title:  "APT-Cacher NG"
description: Creating a local Cache of Ubuntu, Debian and Linux Mirrors. 
date: 2025-03-17 20:03:00 CST
layout: post
categories:  [homelab, cache]
tags: [cache, APT Cacher NG, linux, debian, ubuntu, linux, proxmox, lxc]   # Tag names should always be lowercase
permalink: /APT-Cacher-NG/
pin: false
toc: true
---

#  APT Cacher NG - About and "How To"

## Overview of APT cacher NG
APT-Cacher-NG is designed to cache Ubuntu, Debian and other Linux distrobutions and packages locally.  When one of your machines updates, those updates are stored here.  The next machine that is the same or similar can pull from the cache locally, instead of going out to the internet again. 

## My Pupose & Goals
1. Quite honestly, my main purpose was becasue it seemed like fun to do.
2. It does speed up package downloads, but my internet is good, that really isnt a big deal for me.
3. We are helping Linux, being a good steward of the internet.  If we all do this, that will be less download bandwidth on these distro's.  That will allow them to designate resources elsewhere than handling all the requests.


[ANCHOR LINK TEST](https://vscode.dev/github/TheColetrain/thecoletrain.github.io/blob/main/_posts/draft-2025-03-17-APT-Cacher-NG.md#L24)

## Reccomendation.  Should you do this on your server?
> ### Short answer is YES! (if you know you are "doing this" and need a guide, skip over the rest of this section and get to the "How To area".)
- I will guide you through a "basic" method, this method will have you set up and running in minutes!  Roughly only a few *copy pasta* steps to get APT Casher NG running!  The basic method is so easy, even I can do it. So for the time spent to get anything done is a WIN.  Amount Cached / Time Spent = Winner Winner Chicken dinner.
- I will also then advise of the advanced options and "tweeks" if you want to mess with it further.  If you want it to be as efficient as possible.
> ### The long answer is maybe...
- **Phase 1** If you do the short initial version that I will propose, your cache percentages will not be that significant.  (My personal data will be below)  i.e. you won't cache everything. The tradeoff is how EASY this first version is.  So, you can set up a LXC that caches using scripts and copy/paste in minutes, and if it caches anyting at all... that's a win!  The LXC will take very little resources and not that much storage, and you lost little time.... = win.
- **Phase 2** If you go to the next phase, you can precache a little more, wont take any more CPU or RAM, but it will take a couple Gig's of storage.  Not that much harder.  Once more copy/paste, and press a GUI button.
- **Phase 3** Phase three gets a little tricky.  This is where you are "going for it"  Trying to cache everything under the sun and satisfy all of your obsessive compulsive desires. I tried this level and got sick of it, turned it off.  This involves having updates fail, and then going in to the settings and updating them to resolve.  Quite honestly, I dont much know what I am doing, perhaps someone with a little knowlege would say *"It's so easy, you dont know what you are talking about,"* and they would be Right!
> ### This wont cache HTTPS, it will only cache HTTP. 