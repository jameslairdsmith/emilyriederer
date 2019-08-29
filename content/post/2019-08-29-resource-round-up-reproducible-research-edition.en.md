---
title: 'Resource Round-Up: Reproducible Research Edition'
author: Emily Riederer
date: '2019-08-29'
tags:
  - resources
  - workflow
slug: resource-round-up-reproducible-research-edition
---

I frequently talk, think, and tweet about how open science principles apply to data analysts and scientists in industry. However, despite my interest in reproducibility, my process for sharing my favorite articles on this topic has been anything but reproducible -- repeatedly searching my browser history, past "Sent" mails, or simply typing out the same summaries over and over. 

Going forward, this post serves as a brief annotates bibliography for some of my favorite reads. Did I miss something? Please let me know!

There is little to say in way of introduction that is not already covered eloquently in the links below. However, I'll share just a few words of context on why this issue interests me, outside the walls of academia. Like research scientists, industrial data users are often more incented to deliver quick business wins and use their knowledge to provide actionable and domain-specific insights. *How* this work gets done often gets less attention.

The consequences of in industry may be less dire (e.g. inability to reproduce an AB test on click-through rates versus clinical trial results), but they are no less tangible. The lack of building sustainable tools keeps knowledge siloed within teams and leads to a lot of unnecessary makework. However, despite the obvious benefits of working in code-based, shareable, and reproducible ways, prioritization ("always time to do it again; never time to do it right") and training can be persistent disincentives for action. 

Fortunately, the scientific world has a headstart on solving these problems and figuring out which computing practices deliver practitioners the most bang for the buck. For more on that, keep reading. 


# Practical Approaches

[**Good Enough Practices in Scientific Computing**](https://arxiv.org/abs/1609.00037)    
Greg Wilson, Jennifer Bryan, Karen Cranston, Justin Kitzes, Lex Nederbragt, Tracy K. Teal

[Data Carpentry](https://datacarpentry.org/) offers two-day workshops on reproducible statistical computing essentials (e.g. R, python, SQL, git, etc.) to scientific researchers and shares all their resources free and open source online. This article, written by a number of their driving forces, opens with a irresistible introduction:

>Two years ago a group of researchers involved in Software Carpentry and Data Carpentry wrote a paper called 'Best Practices for Scientific Computing'. It was well received, but many novices found its litany of tools and techniques intimidating. Also, by definition, the 'best' are a small minority. What practices are comfortably within reach for the 'rest'?

More simply, research scientist and industry analysts alike *should* use reproducible practices. Many probably *want* to. However, both groups are incented to prioritize answering a research / business question over changing the way they work. The revelation that reproducibility isn't "all or nothing" but a spectrum of incremental changes one can adopt is enticing and reassuring to domain experts with limited computing experience.

The article proceeds to provide common-sense recommendations and a how-to guide in six main categories: data managament, software, collaboration, project organization, tracking changes, and writing manuscripts. From an industry perspective, my very favorite is "Project Organization". Without typing a line of code, any group can adopt a shared, common-sense file structure, and this small tweak can has massive gains in making past work more discoverable and re-usable.

[**Opinionated Analysis Development**](https://peerj.com/preprints/3210/)    
Hilary Parker

Similiar to "Good Enough Practices", this article surveys motivation, methods, and tools for reproducibility, and provides concrete advice for those looking to get started. Generally, I find it is written in an even warmer and more approachable way for business audiences, probably influenced by Hilary's experiences at Etsy and StitchFix. For example, it invests more time motivating the goal of reproducibility whereas "Good Enough", geared more towards research audiences, is able to take that as more of a given. Additionally, while "Good Enough" intentionally stays mostly language agnostic (Data Carpentry trains in R, python, and other languages), Hilary references many specific R packages to help implement each recommendation.

Recommendations in this piece are broken down into three categories: reproducible and auditable, accurate, and collaborative. This framework is helpful for new users to triage which computational practices are most lacking from their current workflow.

Typically I pick between this and "Good Enough" depending on the audience and feel confident either will be a great call to action.

## On Getting to Scaling 

[**rOpenSci Packages: Development, Maintenance, and Peer Review**](https://ropensci.github.io/dev_guide/)    
Brooke Anderson, Scott Chamberlain, Anna Krystalli, Lincoln Mullen, Karthik Ram, Noam Ross, Maëlle Salmon, Melina Vidoni

[rOpenSci](https://ropensci.org/) curates and maintains a collection of R packages that support various aspects of open and reproducible research. It accomplishes this feat by a fine-tuned set of processes and standards that enable an army of volunteers to make short-term, modular contributions. This effective mobilization of the community provides sustainable oversight without taxing too much of any single contributor's time or resources.^[Earlier this year, I had a great experience taking part in this process as a review of [tradestatistics](https://github.com/ropensci/tradestatistics)]

rOpenSci is a fascinating case study of intentional infrastructure and operations creating an extremely high-functioning organization. However, rOpenSci is not just an aspirational gold-standard. Their "rOpenSci Packages" ebook describes the practices which has helped them succeed and contains much concrete advice for other open-source or innersource aggregators to use.

The book is their guide of advise for designing, developing, reviewing, and maintaining R packages. Beyond a mere checklist of rules or style guides, it contains much practical advise and wisdom for simultaneously sustaining open source tools and their surrounding communities. 

[**Understanding the InnerSource Checklist**](http://innersourcecommons.org/checklist/)    
Silona Bonewald, PayPal

"InnerSource" is the corporate world's term of choice for reproducibility and "open" (within the bounds of that company) source.^[Clearly, two movements about open knowledge sharing and collaboration must be developed separately under different names. [Obligatory xkcd](https://xkcd.com/927/)] This guide from PayPal confronts head-on the challenges of building and InnerSource culture and the necessary structure for it to succeed in an enterprise setting.

While some of this book pertains more to software development, two ideas of particular resonated with me from an analytical tooling perspective: the Trusted Commiter role and of passive documentation. 

The discussion of the Trusted Commiter focuses largely around incentives for internal maintainers. Maintainer burnout is a common phenomenon in open source. In InnerSource, this can be further compounded by traditional performance management structures not being fully prepared to understand and reward the contributions of internal maintainers versus their peers doing glossy new projects. PayPal suggests rotations in and our of these roles at fixed durations.

Passive documentation is another challenge imported from the open source world and exacerbated in the corporate setting. The key question here is how is knowledge from helping a userbase captured over time? In the "wild", we have forums like StackExchange which make past questions easily discoverable. However, InnerSource risks more of this help moving to private messages or the proverbial watercooler. To mitigate this, the book recommends being proactive about using formal channels of communication like Slack.

## Big Picture Perspectives

[**Setting the Default to Reproducible**](http://stodden.net/icerm_report.pdf)    
Victoria Stodden

[Victoria Stodden](http://web.stanford.edu/~vcs/index.html), currently an Associate Professor at the University of Illinois Urbana-Champaign's School of Informatics, is one of the main "faces" of computational reproducibility. I've enjoyed many of her talks, slides, and papers on the topic, and would happily recommend any of them.

The language in this article is more pedagogical than any of the others linked here, so this isn't the most engaging introductory read. In fact, I tend to recommend it purely for the Appendix which provides a taxonomy of different levels of reproducibility. Stodden's spectrum of reproducibility is a useful benchmark to created a shared language and common yardstick for how reproducible your own or your group's work really is.

The five-level system ranges from reviewable (methodology described) to fully open and reproducible. From an industry perspective, I imagine there to be a sixth level of being "extensible" -- that is, open and reproducible work designed in a way conducive to future addition and modification.^[For example, on [episode 67 of the Data Stories podcast](https://datastori.es/67-ggplot2-r-and-data-toolmaking-with-hadley-wickham/), Hadley Wickham discusses how concerted efforts to make `ggplot2   more extensible paid massive dividends]

[**Everything Hertz Podcast: #69 Open Science Tools with Brian Nosek**](https://everythinghertz.com/69)

For the more podcast-inclined, Everything Hertz is a fun, irreverent conversation that captures the zeitgeist of the open science movement. This episode is especially relevant as the hosts are joined by guest Brian Nosek, a social psychology professor and the cofounder and director of the University of Virginia's Center for Open Science. 

This clip assumes listeners have more background knowledge on the "reproducibility crisis" and the open science movement than the readings listed above. Also unlike the other readings, its far less tactical with no specific, actionable recommendations on the *technical* side of getting started. However, it is still an essential piece of an open science "starter kit" due to its thoughtful discussion of the real barriers to adoption. 

Nosek spends a good deal of time examining the sociocultural and technological infrastructure needed for change to occur: common acknowledgment of the problem and appropriate change-making institutions. The first is relatively easy to come by, both in science and business; it's easy to look at what's in front of us and see its flaws. The latter is much harder. Nosek discusses the criticality of both engineering the right technological infrastructure to enable adoption of better practices (such as the [Open Science Foundation](https://osf.io/) has provided) and reshaping incentives so following new processes is attractive (or, at minimum, not destructive.)

