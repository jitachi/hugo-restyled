+++
title = 'I asked Claude to restyle my website'
date = 2026-09-28
draft = false
summary = "One conversation, a new repo, a new Railway service, and a website that finally looks like somebody cares about it."
section = "posts"
category = "Lil-essays"
featured_image = ""
+++

I've written before about how hard it is for me to work on this website. It's a chore, it's PR, it's the thing I'll do "next weekend." So this time I tried something different: I opened Claude for the first time and asked it to do the whole thing for me.

The request was roughly: go to my Railway workspace, find the website project, make a new service called "hugo restyled," copy my Hugo repo into a new GitHub repo, and restyle it without touching the original.

That's a lot of different systems in one sentence. It did all of it.

###### What actually happened

- It checked which Railway account it was connected to and listed my workspaces before doing anything.
- It found the website project and noticed there was already a service with an almost identical name. Instead of steamrolling it, it told me and left it alone.
- It cloned the repo and read the theme: the layouts, the CSS, the fonts. It also spotted a bug I didn't know I had. In system dark mode the page background was, and I quote the stylesheet, `red`.
- It started a local Hugo server, looked at the site, and wrote the new styles.
- It checked its own work in a browser: desktop, dark mode, a phone-sized screen, and whether anything scrolled sideways. When the nav underline showed up under the wrong item, it fixed that too.
- It created a new GitHub repo, pushed the changes there, blocked pushes to my original repo, and wired the new repo up to a new Railway service.
- It waited for the build, read the deploy logs, and opened the live URL to confirm it worked.

The whole thing took about as long as a coffee.

###### The design

Honestly, the part I expected to hate. Instead it went through what was already in the repo and used it. The Recife serif I had been using for body text is now the big display face, JetBrains Mono does dates and labels, and there's a warm paper background with a terracotta accent. The writing page is a numbered index. It even dug up an old hero line I had written and never used, and put it back on the homepage.

Is it exactly what I would have designed? No. Is it better than the page that said "test" in giant letters? Absolutely.

###### Railway is cool

I'm biased, I know. But this is the part that made it feel like magic: the new site isn't a screenshot or a mockup. It's a real service. Railway pulls the repo, runs Hugo, and serves the result, and every push to `main` redeploys it on its own. This post is proof. I asked for it, it got committed, and a minute later it was live.

Having tools that an agent can actually drive (a CLI, an API, readable build logs) turns "please help me with my website" from a weekend into a conversation.

###### So

The best excuse to write is having something to write about. Turns out the best way to work on my website is to not work on it, and just ask.
