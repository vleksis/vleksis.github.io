+++
title = "Comfortable Development"
description = "Small workflow habits that reduced friction in my day-to-day development"
template = "pages/post.html"
+++

There’s no shortage of material about what software engineers do.
For open source, you can inspect the entire history: commits, pull requests, issues, design discussions.
In academia, you can read papers and blog posts explaining ideas in detail.
In commercial work, you can usually see the final product.

What’s harder to observe is the workflow behind the output: the tiny defaults and habits that shape daily work.
How people navigate code, how they make changes safely, how they avoid repeating the same mechanical tasks, how they keep focus.
Without direct communication, most of those details stay invisible.

I like experimenting with small changes that feel immediately useful. Most experiments don’t stick.
But a few habits consistently reduced friction and made development more comfortable for me over the last two years.
This post is a short list of those habits—nothing revolutionary, just practical.

## Vim and keyboard-first workflow

This isn’t really about Vim itself — it’s about the idea of keyboard-only interaction.
Vim is just a good representative because it’s popular and many IDEs support Vim keybindings.

I genuinely like the feeling of not touching the mouse while coding.

It helps me in a few ways:
- Navigation becomes much faster: you can jump, search, change, and insert with a few keystrokes.
- The touchpad tempts me to scroll, switch contexts, and lose focus.
- Sometimes Vim-like editing is the only practical option (e.g., when SSH-ing into a server to debug, edit configs, or inspect logs).

## Scripts

At some point you notice the pattern:

`Up`, `Up`, `Up`…  
search shell history…  
type the same command again…

That’s usually the moment to stop doing Sisyphean tasks and automate.

However I don’t have much more to say yet - I still haven’t found the right tool or language for my own automation setup.
One rule to mention: don’t preemptively automate everything — it’s easy to spend 10 hours automating a 10-minute task.

For further reading: [this article by matklad](https://matklad.github.io/2026/01/27/make-ts.html)

## Editing pipeline

While reading [Martin Fowler’s *Refactoring*](https://martinfowler.com/books/refactoring.html), I found a simple workflow for changing working code:
**change -> build -> test -> commit**.

The idea is to keep changes small and iterative:
rename a variable, add a parameter, split a function, and so on.

Once you’ve accumulated a set of small, safe steps (or finished a refactor),
you can squash them into a single well-named commit (or keep them separate) and push.

It’s not rocket science, but I didn’t think about using Git that way before.
Now it’s hard for me to work any other way.

## Auto-format on save

Auto-format on save is one of those features that feels small until you get used to it.
Once it’s enabled, you stop thinking about indentation, wrapping, and small whitespace decisions.
Your code becomes consistently formatted, diffs get cleaner, and reviews focus more on substance than style.
I try to treat formatting as a background process: write code, save, let the formatter do its job.
