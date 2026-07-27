---
title: "blog --init"
description: "I rebuilt my whole website instead of writing a blog post."
pubDate: 2026-07-27
tags: ["meta", "ai-agents"]
---

If you don't know me, I need to tell you one important thing about myself: I overthink, and then I ~~ruminate~~ think some more.

And if you're just like me, you'll understand why and how publishing my personal blog has been on my to do list for the longest time

I've had multiple attemps on personal blogs in the past 15 years, but last week I was on a team offsite and the goal was to get something shipped even if it wasn't perfect. I've always wanted to redo my website in a way that I liked, so I made that into my goal. It's empowering disconnecting from the idea that something has to be perfect for you to ship it. I always tell that to the new folks on my team, it was time for me to walk the talk.

So for the sake of sharing knowledge (which is also part of my job, and that I genuinely enjoy doing), I'll share a bit of the process here

I had a [Hugo](https://gohugo.io/) page deployed on [Amplify](https://docs.amplify.aws/) since 2021. Since then, it has worked as an online "business card" with my name and socials. No blog posts. Just the process of building something with a new technology for the sake of it, and then never touching it again (can anyone relate?)

It has also been two years since I was finally able to purchase ana.dev (by legitimate means, mind you. I had a yearly calendar reminder set on the domain expiration date). It's a really cool domain and I did get a warning that it was trademarked, so I really hope All Nipon Airways never decides to release their public API.

I wanted to use [Astro](https://astro.build/) because everybody has been talking about it, [add list of cool Astro features here], and it's supposed to be good for blogs, seo (and not an overkill apparently).

Since I remain a proud developer my process is: 1/ Connecting my agents to docs through MCP servers 2/ Ask it to teach me how to do things and explain why 3/ Scolding them when they try do it themselves. I insist on running commands myself and exercising my brain in the process instead of just mindlessly pressing `"Accept"`. If I'm doing the right thing or not, only time will tell.

I've been using [Kiro](https://kiro.dev) (previously Amazon Q Developer) for the past two years because as an AWS Developer Advocate I'm a big believer of eating your own dog food. For this exercise though, I decided to use my personal computer and personal subscription for Claude to see what all the kids have been raving about. It was fun, but the part where I'm fighting and getting frustrated with the agent remains the same.

What surprised me positively was Claude Design. It's finicky but it helped me bring to life the vision that I had in mind even though I lack the design skills for it (I also fought with it a bunch and spent most of the promotional credits I had on my account on the hopes that Fable 5 would make me a great designer -- it didn't).

So Claude Design worked on the design, I brought the HTML/CSS mocks to Claude Code and it helped me build the Astro pages. I'm not 100% happy with the design yet, but I had a deadline to get this out into the world.

Now it was time to deploy. I deleted every file of my previous blog and just went for it. For some reason, even though I deleted amplify.yaml, Amplify still had the old build settings configured and it was trying to deploy a Hugo website (spoiler: it didn't succeed).

Again, because I distrust the baseline technical knowledge of models, I used the AWS MCP server to debug and fix it. You can use it too with no auth (and no AWS account) if you want, here's the simple config:

```json
{
  "mcpServers": {
    "aws": {
      "url": "https://aws-mcp.us-east-1.api.aws/mcp"
    }
  }
}
```

With the page live, I could no longer postpone what I had been postponing for the whole weekend with the excuse of re-building the blog: I had to write the first blog post.

We have so much AI generated ~~slop~~ content out there, that this feels like the perfect excuse to force me to write things here myself so my brain doesn't atrophy (I had to manually search for how to write this, my first attempt was "attrofiate"). So as a challenge to myself, I typed every character you see here (and I am solely responsible for every typo as well).

Worse comes to worst, all my babbling will be used to teach agents to write like me in the future.

Working backwards from doing something that you like and that you want to see come to live, comes this blog with tiny easter eggs that makes it feel like it's mine. This is a work in progress. I might add or remove things in the future, but at least it's shipped.
