---
layout: post
read_time: true
show_date: true
title: "When AI Surpasses Expectations"
date: 2024-09-27
img: posts/20240927/test-lines-changed.png
tags: [ai augmented dev, software engineering, higher level dev, LLM, productivity, coding]
category: technology
author: Adam
description: "Discover how Claude Sonnet 3.5, an AI-powered assistant, enhances software development by not just following instructions but making insightful improvements. A deep dive into AI-augmented development and its impact on productivity."
excerpt: "Claude Sonnet 3.5 exceeded my expectations by not only implementing features in my Higher Level Dev Kit but also improving them with unexpected optimizations. Here's how AI is transforming software development by increasing speed, insight, and efficiency."
---
As I continue developing the Higher Level Dev Kit, I am constantly amazed by how **Claude Sonnet 3.5** not only executes my ideas but often improves upon them in ways I hadn't anticipated. Let me share a recent experience that truly highlights the transformative power of AI in software development.

## Capturing the Essence of Each Commit

I recently added a feature to my toolkit that captures the essence of each commit in a JSON file. This file is stored in the target repository under a `.hldk/specs` directory, effectively creating a history or story of the repository's development. The idea was to have a structured way to document changes, making it easier to track progress and understand the evolution of the codebase.

## Tracking Test Lines Changed

Building on that, I wanted to differentiate between changes made to production code and test code. Specifically, I aimed to track `testLinesChanged` — the number of lines changed in test files as opposed to production files. Adding this metric will allow us to track the relative cost of changes to test code as opposed to production code

## The Git Update That Surprised Me

I instructed Claude to implement this feature, and here's the result—the contents of the generated JSON file:

{% highlight javascript %}
{
  "spec": "update mutation entity to add testLinesChanged similar to linesChanged but is only populated if the filePath contains the string \"test\" (any case) otherwise it's set to 0. Update the service and repo as necessary to set testLinesChanged and also add methods for getTestLinesChangedForSession|Request. Also add the flyway migration.",
  "commitMessage": "Add testLinesChanged feature to mutations",
  "stats": {
    "processingMillis": 65294,
    "inputTokens": 100931,
    "outputTokens": 4587,
    "totalTokens": 105518,
    "cost": 0.2786985,
    "linesChanged": 71,
    "currency": "gbp"
  }
}
{% endhighlight %}

## Beyond Expectations

What surprised me was that Claude not only implemented the feature flawlessly in just over 1 minute at a cost of £0.27 but also added an update line to the Flyway migration script to backfill the `testLinesChanged` data in the existing database—a step I hadn't even considered.

Here's the relevant part of the Flyway migration:

{% highlight sql %}
ALTER TABLE mutations ADD COLUMN testLinesChanged INTEGER DEFAULT 0;

UPDATE mutations SET testLinesChanged = linesChanged WHERE LOWER(filePath) LIKE '%test%';

CREATE INDEX idx_mutations_test_lines_changed ON mutations (testLinesChanged);
{% endhighlight %}

By adding this script, Claude ensured that all historical data was consistent with the new feature, allowing for accurate analytics from the moment of implementation.

## The Power of AI-Augmented Development

This experience reinforces the incredible potential of AI-augmented development:

- **Speed**: Tasks that would typically take hours are completed in minutes.
- **Insight**: The AI doesn't just follow instructions—it understands the context and identifies improvements.
- **Efficiency**: With AI handling the heavy lifting, developers can focus on higher-level problem-solving.

## Embracing the New Paradigm

This is not just a one-off occurrence. I've been consistently experiencing similar enhancements while using the Higher Level Dev Kit with Claude Sonnet 3.5. The AI agent:

- Understands the codebase layout and adapts accordingly.
- Replicates coding styles and best practices, ensuring consistency.
- Identifies potential improvements that may not be immediately obvious.

By embracing AI-augmented development, we unlock unprecedented productivity and insight, allowing us to focus on more innovative and creative tasks.
