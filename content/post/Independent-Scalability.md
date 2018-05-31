+++
title = "Independent Scalability"
date = 2018-05-31T11:25:44-05:00
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
Part 4 of my "Responsible Microservices" series went live yesterday!

# Should that be a Microservice? Part 4: Independent Scalability
In the [first part of this series](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind), we laid out a set of principles to help you understand when microservices can be a useful architectural choice. We promised follow-up pieces describing each of the factors in more detail. In the fourth post of the series, we explore independent scalability.

Let’s take a quick spin in our [hot tub time machine](https://twitter.com/ntschutta/status/844366144630931456) and head back to an era before cloud, microservices and serverless computing. Servers were homegrown and bespoke, beloved pets if you will. When developers requested a server for a new project, it would take weeks or months for it to become available.

Years ago, one of my peers requested a development database for our architecture team. It was never going to hold a lot of data, the database would mostly just act as a repository for some of our artifacts. One would think a small, non-production database could be provisioned somewhat quickly. Amazingly, it took an entire year for us to get that simple request fulfilled! Who knows why this was the case. Strange things happen in traditional enterprise IT. But I do know that these kinds of delays incent a raft of undesirable behavior.

These extended lead times forced us to make capacity decisions far too early. In fact, the very start of a new initiative is when we know the least about what our systems would actually look like under stress. So we’d make an educated guess. This guess would be based on the worst case scenario. Then, we’d double it, and add some buffer. (Plus a little more just in case.)

And while this meant we often heavily overprovisioned infrastructure (and overspent), that was still a good outcome for organizations. After all, adding capacity after the fact was just as painful.

## Monoliths and Traditional Infrastructure: Two Sides of the Same Coin

It wasn’t just our initial server setup that suffered in this era though. Static infrastructure, combined with our old friend the monolithic application, made it nearly impossible for us to deal with unexpected demand. Even if we had a good understanding of what our systems needed under normal circumstances, we couldn’t predict when a new marketing campaign or a shout out from an influencer would send thousands (or millions) of hungry customers to our (now) overwhelmed servers.

Things were no better for Ops teams running our data centers. It could take months to add additional servers or racks. Traditional budgeting processes made it very difficult to add capacity in any kind of “smooth” manner. Instead operators were forced to move in a stepwise fashion relying on (at best) educated guesses about the shape of future business demand.

While this approach was logical at the time, it meant many organizations had massive amounts of unused compute resources sitting idle nearly all of the time. Single digit utilization numbers for servers were common. Business units were paying for unused capacity every month just in case a surge or spike in demand occurred. While this may have been an acceptable tradeoff in the past, today, it would charitably be considered an antipattern.

Elastic infrastructure combined with more modular architectures mitigates many of these antipatterns. Today, you can add, and just as importantly reduce, capacity on demand. You can start with a reasonable number of application instances adapting as you learn more about your load characteristics. Working with your business team, you can spin up extra capacity for that big event and then ramp it down after. You can wait until the last responsible moment freeing you to make better decisions based on real data, not hunches and guesses.

Continue reading [Should that be a Microservice? Part 4: Independent Scalability](https://content.pivotal.io/blog/should-that-be-a-microservice-part-4-independent-scalability) on the [Pivotal blog](https://content.pivotal.io/blog).
