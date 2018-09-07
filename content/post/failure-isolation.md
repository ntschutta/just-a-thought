+++
title = "Failure Isolation"
date = 2018-09-07T12:47:29-05:00
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
caption = ""
preview = true

+++
Part 5 of my "Responsible Microservices" series is live!

# Should that be a Microservice? Part 5: Failure Isolation

In the [first part of this series](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind), we laid out a set of principles to help you understand when microservices can be a useful architectural choice. We promised follow-up pieces describing each of the factors in more detail. In the fifth post of the series, we explore failure isolation.

Digital products don’t live alone. Every piece of tech we use today interacts with something else. The same is true for the custom software we write. Each bit of code works as a part of a larger whole. It’s just one piece of a system that executes a business process. It is right there in the name - “microservice” implies interdependence with other services!

Monoliths have plenty of dependencies, too. It’s common for monoliths to integrate with an aging third-party application that you don’t control. Here, the developers at your company decided to wire up these two systems with [baling twine and duct tape](https://xkcd.com/1988/). These engineers weren’t masochistic. They did the integration for good business reasons, most likely to provide more complete information or a better user experience.

These integrations are a fact of life in software development. You should expect to have integrations between services that were never designed to work together. You should also expect that external services are unlikely to meet your [service level objectives](https://landing.google.com/sre/book/chapters/service-level-objectives.html).

When a downstream dependency fails, it’s tempting to point the finger at a poorly architected piece of technology. But your customers don’t care about excuses. They just want to interact with your software, quickly and easily, then get on with their day.

When you need to protect your systems from failures you can’t control, microservices are a great option. Why? Refactoring the functionality in question into microservices allows you to isolate that dependency from the rest of your application. More importantly, you can protect your SLOs by building proper failover mechanisms.

## Get Started with an Architectural Review

Odds are, you have a pretty good idea of what aspects of your system will benefit from failure isolation. But don’t assume you know all the dark corners. Take the time to perform an architectural review. Gather all your subject matter experts together - developers, architects, and site reliability engineers. Draw up the architecture. You don’t need any formal architectural artifacts. A whiteboard works really well. Make sure to ask and answer questions like:

* What systems does the application talk to?

* How do they integrate?

* Is it a direct call or do you go through a proxy layer?

* What availability level can you expect from those systems?

Continue reading [Should that be a Microservice? Part 5: Failure Isolation](https://content.pivotal.io/blog/should-that-be-a-microservice-part-5-failure-isolation) on the [Pivotal blog](https://content.pivotal.io/blog).
