---
title: rOpenSci and the jobs a package does
author: Emily Riederer
date: '2019-12-31'
draft: true
tags:
  - pkgdev
  - rstats
slug: the-jobs-a-package-does
---

Back in January, I was invited by [rOpenSci](https://ropensci.org/) to review [Mauricio Vargas](https://twitter.com/pachamaltese)' [`tradestatistics`](https://ropensci.github.io/tradestatistics/) package. rOpenSci is an organization which I benefit from substantially^[I am a big fan of many rOpenSci maintained packages and also have applied many of their processes to personal and professional projects], respect greatly^[Their ability to breakdown tasks and solicit short-term, manageable community contribution is a case study for effective leadership in open source or enterprise], and discuss frequently^[For example, see [this post](https://emilyriederer.netlify.com/post/resource-round-up-reproducible-research-edition/)], so I immediately jumped at the chance to get involved. Initially, my motivation was to "give back" to the organization and community. However, an unexpected benefit was gaining a new perspective on R package design and development. 

rOpenSci's [robust infrastructure and review processes](https://devguide.ropensci.org/) encouraged me to closely examine and evaluate the *same* package from both the perspective of a "pure user" and a "pure maintainer". In most cases, an individual only has one of these relationships with any given package. Even where the author/maintainer is a user, they are blind to design choices that may confuse other users.^[For example, in Hadley Wickham's [London R talk, 'Tidyverse: the greatest mistakes'](https://www.youtube.com/watch?v=vYwXMnC03I4&feature=youtu.be), Hadley describes how `tidyr`'s `spread()` and `gather()` function names seemed intuitive to him but cryptic to many users]. 

Around the same time, I also learned about a popular framework in product management: the ["jobs to be done"](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done) (JTBD) theory of strategic innovation.^[One good introduction can be found in [this episode](https://app.stitcher.com/splayer/f/97106/63775442) of the Masters of Product Management podcast.] JTBD conceptualizes products as existing to serve the functional, social, and emotional jobs of a customer. Extending the "jobs" metaphor, product selection is a "hiring process". Implications of this include thinking more broadly about competitors^[The standard example here is a milkshake a commuter might pick up on their way to work. If the job this is fulfilling is to help someone stay alert and engaged while sitting in rush-hour traffic, the competitor set isn't just other beverages like coffee but could include entertainment like listening to the radio] and understanding that the same product may fulfill different "jobs" for different consumers. 

The review process and JTBD collided in my mind and made me wonder: What are the jobs that an R package does for both a user and a maintainer? What qualifications should one look for when "hiring" an R package? In this post, I'll briefly describe the rOpenSci review process, jobs to be done, and what I learned about designing packages to meet both user and maintainer needs. 

## The Review Process

Before I describe what I learned, I'll briefly explain the review process. Anyone who is interested can see this play out on the [GitHub issue](https://github.com/ropensci/software-review/issues/274).

I reviewed `tradestatistics`, a wrapper for the [Open Trade Statistics API](https://tradestatistics.io/). This API provides access to international commodities trading data. Mauricio Vargas built both the package and API so the two products "play nice" together. This created interesting opportunities in the review process since features could be added to either the package or the core API itself.

rOpenSci's ebook [rOpenSci Packages: Development, Maintenance, and Peer Review](https://devguide.ropensci.org/) guided the review process. It provides clear advice for assessing each user-facing (e.g. package website, documentation, API) and maintainer-facing (e.g. code, dependencies, tests) component of a package.  

## Analytics Tools and JTBD

The jobs-to-be-done framework immediately resonated with me as a useful tool to think about desiging analytical tools. Quite literally, package users typically initiate their interaction with a clear goal or "job" in mind. 

Most users aren't seeking new analytical tools for the pure joy of it. With exageration, an analyst or researcher does not *want* to use a tool at all. What they *want* is to fiinish an assignment, develop a business strategy, or answer a research question. Doing this may require data access, management, cleaning, wrangling, summarization, modeling, visualization, etc. However, their *job* is to *answer a question with data* and likely if many could get to a high fidelity answer *without* a tool-intensive process (hypothetically without trading off quality, autonomy, etc.), they would opt to do so.

This is a humbling realization for a package developer or many engaged members of the R community. Self-selected package developer tend to have a passion for tools themselves. Consider simply monthly [RViews](https://rviews.rstudio.com/2019/09/26/august-2019-top-40-r-packages/) posts curating top new packages to explore and the [CRANberries](https://twitter.com/CRANberriesFeed) feed to identify any new developments. However, this passion is mostly orthogonal to the true job of a package.

## Hiring an R Package as a Maintainer

Determining the jobs required by a package developer leads to the bigger question: why do authors develop packages at all? Of course, there are many different reasons to build packages. In the open science context, I would argue that the key jobs are:

- teaching / enabling someone else to do a task that the developer has already done
- evangelizing a new method that the developer has created

To that extent, a package is like an extension of the developer: *"If I had infinite time and resources, I could come sit down with you at a table in help you figure out the code to do that thing I did. But I don't. So, here's my package."*"





- maintainers have needs to because maintenance is an active not passive state
- trusted report / colleauge
- teach hwen not around (vignettes / docs)
- work independently (answer questions well in docs)
- not break & escalate issues (well tested)

## Hiring an R Package as a User

So, if users are not looking to packages for sheer entertainment value, what are they seeking? 

- does what i need and doesn't have unexpected behavior
- easy to learn
- opinionated (workflow vs random code)
- plays nice w broader ecosystem

## Closing Thoughts

Of course, my thoughts above are intentionally painted in broad brush strokes. Of course, users should care about how sustainable packages are, and maintainers should care about an intuitive user experience. My point here is not to draw a line between these groups. Quite the opposite, when one is playing either of these roles, it can be easy to lose site of the other. Conceptualizing needs as part of two "extreme" personas hopefully can help some users and developers remember to "try on" the other role on occasion.

More importantly, reviewing for rOpenSci helped me think different and more critically about using and building R packages. No matter where you are in your R journey, the opportunity to engage in a thoughtful, open discussion about an R package in a caring community may also give you new insights or inspirations. If this sounds appealing, please also [volunteer to review](https://ropensci.org/onboarding/).
