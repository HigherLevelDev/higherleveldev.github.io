---
layout: post
read_time: true
show_date: true
title: "Intro to Higher Level Development"
date: 2024-09-22
img: posts/20240922/dall-e-headline-future.png
tags: [ai augmented dev, software engineering, higher level dev, LLM, productivity, coding]
category: technology
author: Adam
description: "Discover how AI-powered Software Engineering Agents are transforming software development, allowing developers to code primarily through natural language."
excerpt: "Learn how AI-augmented development is changing the landscape of software engineering, making it possible to develop at a higher level using natural language instructions."
---
When Anthropic released Claude Sonnet 3.5 on Friday, June 21st, 2024, software development changed forever.

Just a few days later, on Monday the 24th, I was made redundant from the fintech payments company where I had been working for over six years, as it prepared to shut down. In hindsight, I believe this turn of events was quite serendipitous.

I had already been experimenting with ChatGPT and other large language models (LLMs), trying to leverage them to become more productive in my role as a backend engineer. 
But with Claude Sonnet 3.5, we finally had an LLM capable of writing decent, reliable code that was mostly bug-free. 

This changed everything.

Given six weeks of gardening leave, I decided to immerse myself in this new world instead of searching for another job. 
I started by dabbling in Python and learning about frameworks like LangChain and LangGraph. 

By pasting existing code into Claude and asking it to build the next part, then incorporating that back into my IDE, I managed to build a Python-based server running some agents and a rudimentary web app to interact with them.

One of the agents I developed was called the System Improver Bot. It functioned by providing it with the root folder of a code 
repository (I simply pointed it to itself) and sending the tree of source file names to Claude along with instructions on what 
to do next. 

By equipping Claude with a read_file tool, it could decide which files it needed to read to understand the codebase before generating new code. By parsing the responses, I could automatically save the generated code back to the file system. 

I no longer needed the Claude UI at all, and my productivity skyrocketed. It didn't matter that I didn't really know Python or that I was a complete novice at web development. 

<b>I'm now developing in the English language - this is Higher Level Development.</b>

After 25 years of building backend systems in the Java ecosystem, I've finally become a 10x Engineer. And it's a lot of fun. And any other developer can do the same with access to the right tools and a few days to get up to speed on how to direct the agent.

It's a new paradigm: you develop one small specification at a time.
For example:

{% highlight markdown %}
Add a new person module to the system. 
The Person entity needs properties:id (UUID), title, firstName, 
lastName, dob (string), createdAt (timestamp). 
Add the appropriate repository with the usual methods, 
the service and controller, and all the necessary DTOs and unit tests. 
Also, add a Flyway migration for the new person table.
{% endhighlight %}

This task usually involves a lot of boilerplate code and might have taken at least an hour or two in the past. But a Claude-powered coding agent can do an excellent job of this in about two minutes. 

Claude can see the codebase layout and examine other modules in the system. It learns how entities are structured and replicates the same style and tooling.

I’ve been using this methodology over the past (checks notes…) 2 weeks (!?!) to build a new production-ready version of my toolkit.. this time the tech stack is a NestJS/Node server and a Vue3 web UI.

Here's a video of the new tool implementing the above mini-spec in a Java Spring Boot git repo:

<div class="video-container" style="position: relative; padding-bottom: 56.25%; padding-top: 30px; height: 0; overflow: hidden;">
  <iframe 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" 
    src="https://higherleveldev.s3.eu-west-1.amazonaws.com/HLDKAddPersonModule-opt.mp4" 
    title="Video player" 
    frameborder="0" 
    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
    referrerpolicy="strict-origin-when-cross-origin" 
    allowfullscreen>
  </iframe>
</div>

At the end, it also runs the tests—including the newly created unit tests—and verifies that everything is working. If it wasn’t working then it would iterate fix -> test -> fix --> test until everything was working correctly.

<img src="{{ site.url }}/assets/img/posts/20240922/tests-passed.png" alt="All tests passed">

Generating new code like this is fairly straightforward, but Claude Sonnet 3.5 also excels at making edits to existing code and even performing refactorings of limited size. As a general rule, if I anticipate changes to more than ten files at once, I tend to break the work down into smaller specs and iterate through them one at a time.

The toolkit I've developed will automatically commit each set of changes to Git with a suitable commit message. If you're not satisfied with the changes, a simple "undo" is enough to revert them.

Though the example uses a Java Spring Boot application, the Higher Level Dev Kit is designed for versatility across any codebase. Whether you're working in Node.js, .NET, Python, Go, building Android or iOS apps, or using React, Angular, or Next.js, the toolkit seamlessly adapts to your stack. By allowing developers to hand off coding tasks to an LLM agent through concise specs written in English (or other native languages), it transforms how you approach development, letting you focus on higher-level problem-solving while the agent handles the details.

This is how I do all my development now. There's no going back or putting the genie back in the bottle.

<b>This is the way.</b>

Based on what I've learned and the excellent results I've been seeing so far using this approach, I'm starting my own boutique consultancy, offering to help companies radically improve their developer productivity by adopting this same toolkit and workflow.

My goal is to build a sustainable business, fostering long-term relationships with a small set of software teams, so they can leverage the Higher Level Dev Kit to supercharge their development in a totally affordable way.

Together, we can improve the toolkit, incorporate the latest and greatest LLM models (o1 anyone?), and be at the forefront of AI-augmented development.

<a href="https://www.higherleveldev.com/dyp-offer?utm_source=blog&utm_medium=linkedin&utm_campaign=intro-to-hld" target="_blank">Early Bird Offer till end of October: Book your free consultation now!</a>