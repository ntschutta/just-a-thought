+++
title = "Responsible Microservices"
date = 2018-09-07T11:46:02-05:00  # Schedule page publish date.
draft = false

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
# time_start = 2018-09-07T11:46:02-05:00
# time_end = 2018-09-07T11:46:02-05:00

# Abstract and optional shortened version.
abstract = "These days, you can’t swing a dry erase marker without hitting someone talking about microservices. Developers are studying Eric Evan’s prescient book Domain Driven Design. Teams are refactoring monolithic apps, looking for bounded contexts and defining a ubiquitous language. And while there have been countless articles, videos, and talks to help you convert to microservices, few have spent any appreciable time asking if a given application should be a microservice. In this talk, I will show you a set of factors you can apply to help you decide if something deserves to be a microservice or not. We’ll also look at what we need to do to maintain a healthy micro(services)biome."
abstract_short = ""

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
# 7 = Conference Talk
# 8 = Workshop  
# 9 = Keynote  

publication_types = ["7"]

# Name of event and optional event URL.
event = ""
event_url = ""

# Length of the talk
duration = "45-90 minutes"

# Location of event.
location = ""

# Is this a selected talk? (true/false)
selected = false

# Projects (optional).
#   Associate this talk with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["architecture", "talk", "conference", "services", "FaaS", "serverless", "k8s", "kubernetes", "docker", "spring", "cloud", "12factor", "microservices", "functions", "trade-offs", "technology", "techniques"]

# Links (optional).
url_pdf = ""
url_slides = ""
url_video = ""
url_code = ""

# Does the content use math formatting?
math = false

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++
### Full Abstract

# Responsible Microservices

These days, you can’t swing a dry erase marker without hitting someone talking about microservices. Developers are studying Eric Evan’s prescient book Domain Driven Design. Teams are refactoring monolithic apps, looking for bounded contexts and defining a ubiquitous language. And while there have been countless articles, videos, and talks to help you convert to microservices, few have spent any appreciable time asking if a given application should be a microservice. In this talk, I will show you a set of factors you can apply to help you decide if something deserves to be a microservice or not. We’ll also look at what we need to do to maintain a healthy micro(services)biome.

There are many good reasons to use a microservices architecture. But there are no free lunches. The positives of microservices come with added complexity. Teams should happily take on that complexity...provided the application in question benefits from the upside of microservices. This talk will cut through the hype to help you make the right choice for your unique situation.

Responsible Microservices is based on my blog series [Should that be a Microservice? Keep These Six Factors in Mind](https://content.pivotal.io/blog/should-that-be-a-microservice-keep-these-six-factors-in-mind) found on the [Pivotal blog](https://content.pivotal.io/blog).
