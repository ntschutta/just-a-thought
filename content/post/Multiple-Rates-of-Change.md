+++
title = "Multiple Rates of Change"
date = 2018-03-01T09:11:58-06:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["architecture", "services", "fundamentals", "Pivotal", "spring", "microservices", "principles", "lessons learned"]
categories = ["blog", "microservices", "lessons learned"]

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
# Use `caption` to display an image caption.
#   Markdown linking is allowed, e.g. `caption = "[Image credit](http://example.org)"`.
# Set `preview` to `false` to disable the thumbnail in listings.
[header]
image = ""
caption = "Should that be a Microservice? Part 2: Multiple Rates of Change"
preview = true

+++
Part 2 of my "Responsible Microservices" series went live last week!

# Should that be a Microservice? Part 2: Multiple Rates of Change

In the [first part of this series](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind), we laid out a set of principles to help you understand when microservices can be a useful architectural choice. We promised follow-up pieces describing each of the factors in more detail. Here’s the first of such posts; let’s explore multiple rates of change.

Recall our Widget.io example, a prototypical shopping app.

We discovered that our Cart and Inventory functions hadn’t been updated in some time. Meanwhile, the Recommendation Engine and Search capabilities are modified frequently.

Splitting those two modules - Recommendation Engine and Search - into microservices would allow the respective teams to iterate at a faster pace. This approach will help us quickly deliver business value.

In this fictitious example, we can simply declare “these modules change a lot.” But that won’t fly in the real world. How do we find parts of our application that evolve at different rates? More specifically, how do we find the components that change far faster than the rest?

Normally, software developers skew logical. But let’s use our emotional and rational brains in concert. Odds are, you have an inkling about the part of your app most likely to benefit from faster iteration. Trust your gut instincts!

But you shouldn’t rely entirely on feelings. We can use our source code management system to give us a “heat map” of our code. With a git repository for instance, we can run git log with a few command line options piped through common Linux tools. We can generate a “top ten list” of most commited files with a command like this:

    git log --pretty=format: --name-only | sort | uniq -c | sort -rg | head -10

Continue reading [Should that be a Microservice? Part 2: Multiple Rates of Change](https://content.pivotal.io/blog/should-that-be-a-microservice-part-2-multiple-rates-of-change) on the [Pivotal blog](https://content.pivotal.io/blog).
