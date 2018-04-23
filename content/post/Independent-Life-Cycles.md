+++
title = "Independent Life Cycles"
date = 2018-04-23T15:48:03-05:00
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
Part 3 of my "Responsible Microservices" series went live earlier this month!

# Should that be a Microservice? Part 3: Independent Life Cycles
In the [first part of this series](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind), we laid out a set of principles to help you understand when microservices can be a useful architectural choice. We promised follow-up pieces describing each of the factors in more detail. In the third post of the series, we explore independent life cycles. Independent life cycles are a larger concept. [Multiple Rates of Change](https://content.pivotal.io/blog/should-that-be-a-microservice-part-2-multiple-rates-of-change), discussed previously, are a subset of this idea. For a variety of reasons, we often find parts of the code that need their own commit to production flow. Let’s consider this dynamic and how microservices help.

A monolithic approach usually hinders our ability to deliver quickly, run A/B tests, and learn from users. Recall our Widget.io example, a prototypical shopping app.

In our hypothetical scenario, our business leadership identified a new opportunity that requires speed to market. A typical monolith wouldn’t allow us to iterate fast enough, so we made Project X its own microservice. Project X has its own code repository and deployment pipeline - and therefore an independent life cycle. This will help us evolve Project X as we learn more about the business opportunity.

## Independent Life Cycles Boost Developer Productivity

But speed to market isn’t the only reason we might want an independent life cycle for a module. We can increase developer productivity too!

Very few developers would say monoliths help them be productive. They slog through dictionary-length developer setup guides. Build times are measured with a sundial. It can take months for a developer to get up to speed on a project. With a smaller scope, a developer can get their head wrapped around a microservice in a day or two. Builds finish in a few minutes (or less). If the build gets broken, engineers know right away and they can take immediate action to fix something.

Smaller code bases also mean testing a microservice can be far simpler too. Tools like [Spring Cloud Contract](https://cloud.spring.io/spring-cloud-contract/) can help us ensure our services are good citizens and play well with others. Don’t bother with the monolith’s 80-hour regression suite. Instead, build a set of fine-grained tests against a microservice that can be executed on every commit. Rather than a “one size fits none” approach to testing, we can bring the right tools and techniques to bear on the individual circumstances of a given microservice. We can subject our microservices to constant scrutiny, instead of a one-off performance test. Imagine how this boosts code quality!

Continue reading [Should that be a Microservice? Part 3: Independent Life Cycles](https://content.pivotal.io/blog/should-that-be-a-microservice-part-3-independent-life-cycles) on the [Pivotal blog](https://content.pivotal.io/blog).
