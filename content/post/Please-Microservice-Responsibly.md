+++
title = "Please Microservice Responsibly"
date = 2018-01-19T16:50:42-06:00
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
caption = "Should that be a Microservice? Keep These Six Factors in Mind"
preview = true

+++
I wrote a post summarizing some advice that [Matt Stine](http://www.mattstine.com) and I used with a client...

# Should that be a Microservice? Keep These Six Factors in Mind

You’re writing more code than ever before. The trick is knowing what should be a microservice, and what shouldn’t.

These days, you can't swing a dry erase marker without hitting someone talking about microservices. Developers are studying Eric Evan’s prescient book [Domain Driven Design](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215). Teams are refactoring monolithic apps, looking for bounded contexts and defining a ubiquitous language. And while there have been countless articles, videos, and talks to help you convert to microservices, few have spent any appreciable time asking if a given application should be a microservice.

There are many good reasons to use a microservices architecture. But there are no free lunches. The positives of microservices come with added complexity. Teams should happily take on that complexity...provided the application in question benefits from the upside of microservices.

## Please Microservice Responsibly

[Matt Stine](https://twitter.com/mstine) and I recently spent a few days with a client walking through some of their applications. The discussion started from a standpoint of "everything should be a microservice" as it often does these days. The conversation stalled as people argued over various implementation details.

That prompted Matt to write a set of principles on the whiteboard. These simple statements guided us the rest of the day. They led us to question every part of the application architecture, looking for places where a microservice would deliver value. The list fundamentally changed the tone of the conversation and helped the team make good architectural decisions.

To rid the world of surplus microservices, we present this list to help focus your efforts. Read through the following principles and ask if the application in question benefits from a given principle. If you answer “yes” for one or more of the following principles, the feature is a good candidate to be a microservice. If you answer “no” for every principle, you are likely introducing [accidental complexity](https://www.amazon.com/Mythical-Man-Month-Software-Engineering-Anniversary/dp/0201835959) into your system.

Continue reading [Should that be a Microservice? Keep These Six Factors in Mind](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind) on the [Pivotal blog](https://content.pivotal.io/blog):
