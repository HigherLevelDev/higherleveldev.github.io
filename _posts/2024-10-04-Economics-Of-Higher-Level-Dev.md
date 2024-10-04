---
layout: post
read_time: true
show_date: true
title: "Not investing in AI Augmented Development is commercial suicide"
date: 2024-10-04
img: posts/20241004/productivity-gains.png
tags: [ai augmented dev, software engineering, higher level dev, LLM, productivity, coding, gartner]
category: technology
author: Adam
description: "Explore how AI is revolutionizing software development, following the path of historic productivity leaps like the cotton gin and the assembly line. This post examines the impact of AI tools on developer efficiency, featuring insights from a recent Gartner report and real-world examples of AI-enhanced coding. Learn about the future of AI-native software engineering and how it's reshaping the role of developers."
excerpt: "The future of software development is upon us, with AI tools delivering productivity gains comparable to historical innovations like the cotton gin and assembly line. Discover how AI agents are transforming the industry, offering up to 50x improvements in coding efficiency."
---

Before Eli Whitney invented the cotton gin in 1793, a worker could clean about 450 grams of cotton per day manually. With the cotton gin, that same worker could process 23 kilograms—a 50x productivity boost. Similarly, Cyrus McCormick’s mechanical reaper, introduced in 1831, revolutionized farming by allowing a single person to harvest up to 12 acres of grain in a day, compared to the half-acre possible with traditional methods—a 24x increase. And then, in 1913, Henry Ford’s assembly line delivered an 8x improvement in automobile production, reducing the time to assemble a car from 12 hours to just 90 minutes.

This pattern of radical productivity increases is now happening in software development. Today, with the right AI tools, developers can boost their productivity by a factor of three to four. In the near future, we can expect this to jump to 10x, and perhaps even 50x.

In previous posts, we’ve seen an AI Software Engineering Agent complete <a href="{{ site.url }}/Intro-to-Higher-Level-Dev.html" target="_blank">two hours of manual coding work in just two minutes</a>. We’ve also explored how <a href="{{ site.url }}/Claude-Surpasses-Expectations.html" target="_blank">human + AI partnerships deliver superior results</a> compared to humans working alone.

### A Seismic Shift in Developer Work Patterns

A <a href="https://www.gartner.com/en/newsroom/press-releases/2024-10-03-gartner-says-generative-ai-will-require-80-percent-of-engineering-workforce-to-upskill-through-2027" target="_blank">recent Gartner report</a> anticipates a seismic shift:

> "AI agents will transform developer work patterns by enabling developers to fully automate and offload more tasks. This will mark the beginning of AI-native software engineering, where most code is AI-generated rather than human-authored."

Philip Walsh, Senior Principal Analyst at Gartner, added:

> “In the AI-native era, software engineers will adopt an ‘AI-first’ mindset, focusing on steering AI agents toward the most relevant context and constraints for a given task. This makes natural-language prompt engineering and retrieval-augmented generation (RAG) essential skills for developers.”

We are entering this era now. These agents are available today and can deliver significant productivity gains immediately.

### Estimating the Cost of Code

To put this into context, I asked Open AI’s new o1-preview model to estimate the cost of each line of code written by a senior engineer earning £80,000 per year. The estimate came out to roughly £2.40 per line of code, based on an average of 50 lines of code per hour and four hours of coding per day (* see Appendix below).

Over the past week, while figuring out how to market my new consultancy business, I’ve also used my dev kit to enhance itself. Here's a screenshot of the new dashboard, showing this week’s work:

<img src="{{ site.url }}/assets/img/posts/20241004/hldk-dashboard-this-week.png" alt="Dashboard Screenshot">

A total of 201 requests this week. The last one? I just made a small adjustment to improve the screenshot:

> Add labels to the period drop down on the dashboard page so value all-time reads as "All Time" in the drop down and similarly for the other values.

This took 25 seconds, cost me 10 pence in Claude credits, and updated eight lines of code.

In total, I’ve spent roughly £50 on Claude this week and updated over 4,000 lines of code. If we use the £2.40 per line estimate, this equates to just under £10,000 in value generated. On average, each request took about one minute and updated 20 lines of code, costing 25p and delivering £50 in value.

Looking back, I’ve likely spent around half of each workday (Monday to Thursday) working on the Higher-Level Dev Kit. That’s approximately 16 hours in total—resulting in 250 lines of code per hour, a 5x increase over the industry average.

Every company with a software development team should be engaging with these AI tools today. Those that don’t will be at a severe disadvantage against those that do.

### The Future of Software Engineering

I’ll leave you with some insightful words from Simon Willison, co-creator of Django:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/uRuLgar5XZw?si=B_wL_MPp2D0yUJX0&amp;start=2817" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

> “... when you combine expertise in using these tools with subject-matter expertise, you can operate at a level far above other people and the competitive advantage you get is enormous”

---

### *Appendix: Calculating the Cost per Line of Code (LOC)

Obviously, this is a very rough estimate - and should be taken with a large pinch of salt.

For a UK-based Senior Back-End Engineer earning £80,000 annually, let’s recalculate the cost of producing each line of code, factoring in total costs to the employer.

#### Total Cost to Employer:
- Base Salary: £80,000
- Employer's National Insurance Contributions (NICs): £9,784.20
- Employer's Pension Contributions (5%): £4,000
- Overheads (20%): £16,000

**Total Cost to Employer** = £110,000

#### Estimating Productive Coding Hours:
- Working Days per Year: 227 (after accounting for leave and holidays)
- Total Working Hours per Year: 1,816
- Time Spent on Coding: 50% of total working hours = 908 hours

#### Lines of Code per Hour:
- Assumed Productivity: 50 LOC per hour

#### Total Lines of Code per Year:
- 908 hours × 50 LOC/hour = 45,400 LOC

#### Cost per Line of Code:
- Cost per LOC = £110,000 / 45,400 LOC = £2.42 per LOC

**Summary**:
A senior engineer costs a company approximately £110,000 per year and produces roughly 45,400 lines of code annually, leading to an estimated cost of £2.42 per line of code.

### Sources:
- UK Government Resources on Employer NICs
- Steve McConnell's *Software Estimation: Demystifying the Black Art* (2006)
- Industry salary benchmarks via Glassdoor and Indeed
