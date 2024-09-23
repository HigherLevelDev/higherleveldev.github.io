---
layout: post
read_time: true
show_date: true
title: "Intro to Higher Level Dev"
date: 2024-09-22
img: posts/20240922/dall-e-headline-future.png
tags: [ai augmented dev, software engineering, higher level dev]
category: opinion
author: Adam
description: "It's become possible to develop software primarily through natural language by working in tandem with an LLM-powered Software Engineering Agent."
---
Software development changed forever on Friday, June 21st, 2024. 

Just a few days later, on Monday the 24th, I was made redundant from the fintech payments company where I had been working for over six years, as it shut down. In hindsight, I believe this turn of events was quite serendipitous.

I had already been experimenting with ChatGPT and other large language models (LLMs), trying to leverage them to become a more productive backend engineer. 
But when Anthropic released Claude Sonnet 3.5, we finally had an LLM capable of writing decent, reliable code that was mostly bug-free. 

This changed everything.

Given six weeks of gardening leave, I decided to immerse myself in this new world instead of searching for another job. 
I started by dabbling in Python and learning about frameworks like LangChain and LangGraph. 

By pasting existing code into Claude and asking it to build the next part, then incorporating that back into my IDE, I managed to build a Python-based server running some agents and a rudimentary web app to interact with them.

One of the agents I developed was called the System Improver Bot. It functioned by providing it the root folder of a code 
repository (I simply pointed it to itself) and sending the tree of source file names to Claude along with instructions on what 
to do next. 

By equipping Claude with a read_file tool, it could decide which files it needed to read to understand the codebase before generating new code. By parsing the responses, I could automatically save the generated code back to the file system. 

I no longer needed the Claude UI at all, and my productivity skyrocketed. It didn't matter that I didn't really know Python or that I was a complete novice at web development. 

<b>I'm now developing in English - this is Higher Level Development.</b>

After 25 years of building backend systems in the Java ecosystem, I've finally become a 10x Engineer. And it's a lot of fun. And any other developer can do the same with access to the right tools and a few days to get up to speed on how to direct the agent.

It's a new paradigm: you develop one small specification at a time.
For example:

<b>"Add a new person module to the system. The Person entity needs properties: id (UUID), title, firstName, lastName, dob (string), createdAt (timestamp). Add the appropriate repository with the usual methods, the service and controller, and all the necessary DTOs and unit tests. Also, add a Flyway migration for the new person table."</b>

This task usually involves a lot of boilerplate code and might have taken at least an hour or two in the past. But a Claude-powered coding agent can do an excellent job of this in about two minutes. 

Claude can see the codebase layout and examine other modules in the system. It learns how entities are structured and replicates the same style and tooling.

I’ve been using this methodology over the past (checks notes…) 2 weeks to build a new production-ready version of my toolkit.. this time the tech stack is a NestJS/Node server and a Vue3 web UI.

Here's a video of the new tool implementing the above mini-spec in a Java Spring Boot git repo:

<iframe width="560" height="315" src="https://www.youtube.com/embed/Wckhd-vIaw4?si=udK7EkIuZZLmjKSU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

At the end, it also runs the tests—including the newly created unit tests—and verifies that everything is working. If it wasn’t working then it would iterate fix -> test -> fix test until everything was working correctly.

Generating new code like this is fairly straightforward, but Claude Sonnet 3.5 also excels at making edits to existing code and even performing refactorings of limited size. As a general rule, if I anticipate changes to more than ten files at once, I tend to break the work down into smaller specs and iterate through them one at a time.

The Higher Level Dev Kit I've developed will automatically commit each set of changes to Git with a suitable commit message. If you're not satisfied with the changes, a simple "undo" is enough to revert them.

This is how I do all my development now. There's no going back or putting the genie back in the bottle.

<b>This is the way.</b>

As a result, I'm starting my own boutique consultancy, helping companies to radically improve their developer productivity by adopting this same workflow.

My goal is to build a sustainable, one-man, business, fostering long-term relationships with a small set of software teams, so they can leverage the Higher Level Dev Kit to supercharge their development in a totally affordable way.

Together, we can improve the toolkit, incorporate the latest and greatest LLM models (O1 anyone?), and be at the forefront of AI-augmented development.

<a href="https://www.higherleveldev.com/dyp-offer?utm_source=blog&utm_medium=linkedin&utm_campaign=intro-to-hld" target="_blank">Early Bird Offer till end of October: Book your free consultation now!</a>
