---
title: 'Resource Round-Up: Reproducible Research Edition'
author: Emily Riederer
date: '2019-12-31'
tags:
  - resources
  - workflow
slug: resource-round-up-reproducible-research-edition
---

Open science and reprducibility are hot topics in the academic world, but I'm often confronted with the disparity between something that is a buzzword in my Twitter feed being a blip on the radar in much of corporate America^[On the *analysis* side of the spectrum]. Industry seems quite taken by the prospect of human-out-of-the-loop automation, but its less common to discuss how data analysts can take *more*, not less, control over their work by embracing reproducible methods.

Even when this need is recognized, duplication of effort seems to be par for the course. In layman's terms, computational reproducibility is a movement around open and accessible documentation and sharing of insight-generating resources. So, there's a certain irony that countless corporate knowledge management solutions and frameworks like InnerSource are being duplicatevely developed without taking advtange of the available resources *about* open science.




This has become one of my pet issues because the opportunity cost is so large. In the academic world, credibility and collaboration are among the biggest benefits of reproducibility. In industry, many of the same concepts -- better knowledge and tool sharing, open peer review, working with code versus graphical user interfaces -- can drive efficiency and employee morale. No one wants to generate the same old [TPS report](https://www.youtube.com/watch?reload=9&v=Fy3rjQGc6lA) month after month. 

As with most of my pet issues, I can be very persistent. Below are a few of my favorite writings on the topic that I'll send to anyone who shows interest (and occassionally those that don't). I find they serve as great introductions to the practical benefits of reproducibility and, even better, offer tangible and easy-to-implement suggestions of how to get there.

## Tactical Approaches

[**Good Enough Practices in Scientific Computing**](https://arxiv.org/abs/1609.00037)    
Greg Wilson, Jennifer Bryan, Karen Cranston, Justin Kitzes, Lex Nederbragt, Tracy K. Teal

This article is written by a number of the driving forces behind [Data Carpentry](https://datacarpentry.org/), an impressive organization which offers phenomenal open-source resources and two-daytraining workshops in statistical computing for researchers. This is very analogous to the struggle of analysts in industry; researchers *should* use reproducible practices and on some level probably *want* to, but at the end of the day, this will always come second to their focus on using data to answer questions in their domain. 

This article is written as an answer to that very concern. To quote "Good Enough"'s irresistible introduction: 

>Two years ago a group of researchers involved in Software Carpentry and Data Carpentry wrote a paper called 'Best Practices for Scientific Computing'. It was well received, but many novices found its litany of tools and techniques intimidating. Also, by definition, the 'best' are a small minority. What practices are comfortably within reach for the 'rest'?

To me, the relevation alone that reproducibility wasn't an "all or nothing" proposition but a series of optional(ish), incremental changes was enticing and made digging into the topic less daunting.

Check out the full article for more specifics on the authors' recommendations, which they summarize as follows:

- Data Management: saving both raw and intermediate forms; documenting all steps; creating tidy data amenable to analysis.
- Software: writing, organizing, and sharing scripts and programs used in an analysis.
- Collaboration: making it easy for existing and new collaborators to understand and contribute to a project.
- Project Organization: organizing the digital artifacts of a project to ease discovery and understanding.
- Tracking Changes: recording how various components of your project change over time.
- Manuscripts: writing manuscripts in a way that leaves an audit trail and minimizes manual merging of conflict.

[**Opinionated Analysis Development**](https://peerj.com/preprints/3210/)    
Hilary Parker

This article has a similar spirit to "Good Enough Practices" in that it provides a survey of motivation, methods, and tools, and provides a lot of concrete advice for those looking to get started. Generally, I find it is written in an even warmer and more approachable way for business audiences, probably influenced by Hilary's experiences at Etsy and StitchFix, and spends a lot of time building up the motivation for its recommendations in a colorful and thought-provoking way. Additionally, while "Good Enough" intentionally stays a bit more language agnostic (Data Carpentry trains in R, python, and other languages), Hilary's recommendations are very concrete and highlight many great R packages to try. 

She outlines the main sections of recommendations as follows:

- Reproducible and Auditable
  + Executable analysis scripts
  + Defined dependencies
  + Watchers for changed code and data
  + Version control (individual)
  + Code review
- Accurate
  + Modular, tested code
  + Assertive testing of data, assumptions and results
  + Code review
- Collaborative
  + Version control (collaborative)
  + Issue tracking

Typically I pick between this and "Good Enough" depending on the audience and feel confident either will be a great call to action.

## Case Study

[**rOpenSci Packages: Development, Maintenance, and Peer Review**](https://ropensci.github.io/dev_guide/)    
Brooke Anderson, Scott Chamberlain, Anna Krystalli, Lincoln Mullen, Karthik Ram, Noam Ross, Maëlle Salmon, Melina Vidoni

I have been fascinated by rOpenSci ever since I first learned about it. This NUMFOCUS-sponsored organization curates and maintains a collection of R packages that support various aspects of open and reproducible research. 

To accomplish this feat, rOpenSci has fine-tuned its processes and standards to mobilize an army of volunteers and allow community members short-term, modular contributions. This provides rOpenSci with the consistent and sustaining fueld it needs without taxing too much of any single contributor's time and resources. 

The key to this is their guide of advise for developing, reviewing, and maintaining R packages. This guide has generally great thoughts on best practices for package design, but more tactically is the one-stop show for package developers and reviewers to onboard themselves to the rOpenSci software review process.^[I recently had a great experience taking part in this process as a review of [tradestatistics](https://github.com/ropensci/tradestatistics)]

This ebook has a ton of practical advise and wisdom for sustaining both open source tools and communities. 

## Big Picture Perspectives

[**Setting the Default to Reproducible**](http://stodden.net/icerm_report.pdf)    
Victoria Stodden

[Victoria Stodden](http://web.stanford.edu/~vcs/index.html), currently an Associate Professor at the University of Illinois Urbana-Champaign's School of Informatics, is one of the main "faces" of computational reproducibility. I've enjoyed many of her talks, slides, and papers on the topic, and would happily recommend any of them.

The language in this article is more academic and pedagogical than the two above, so this isn't the most engaging introductory read. Strangely enough, the reason I like to recommend it is actually for the Appendix in which Stodden provides a taxonomy of different levels of reproducibility. I find Stodden's approach to naming and setting different benchmarks around reproducibility to be an incredibly useful way to start forming a language of discussion on the topic and to have a bar against which to measure. 

For reference, these levels (paraphrased) are:

- Reviewable Research: Methodology described
- Replicable Research: Limited tooling available to some to duplicate specific results
- Confirmable Research: Methods described sufficiently so that main conclusions can be recreated but possibly without access to initial set of tools
- Auditable Research: Data and software preserved so that research can be recreated or audited, but these resources are not neccesarily made public 
- Open or Reproducible Research: Complete data and software are openly available to allow reproduction and extension

[**Everything Hertz Podcast: #69 Open Science Tools with Brian Nosek**](https://everythinghertz.com/69)

For the more podcast-inclined, Everything Hertz is a fun, irreverent conversation that captures the zeitgeist of the open science movement. This episode is especially relevant as the hosts are joined by guest Brian Nosek, a social psychology professor and the cofounder and director of the University of Virginia's Center for Open Science. 

This clip assumes listeners have more background knowledge on the "reproducibility crisis" and the open science movement than the readings listed above. Also unlike the other readings, its far less tactical with no specific, actionable recommendations on the *technical* side of getting started. However, it is still an essential piece of an open science "starter kit" due to its thoughtful discussion of the real barriers to adoption. 

Nosek spends a good deal of time examining the sociocultural and technological infrastructure needed for change to occur: common acknowledgement of the problem and appropriate change-making institutions. The first is relatively easy to come by, both in science and business; it's easy to look at what's in front of us and see its flaws. The latter is much harder. Nosek discusses the criticality of both engineering the right technological infrastructure to enable adoption of better practices (such as the [Open Science Foundation](https://osf.io/) has provided) and reshaping incentives so following new processes is attractive (or, at minimum, not destructive.)

[**Understanding the InnerSource Checklist**](http://innersourcecommons.org/checklist/)    
Silona Bonewald, PayPal

"InnerSource" is the corporate world's term of choice for reproducibility and "open" (within the bounds of that company) source.^[Because, naturally, two movements about open knowledge sharing and collaboration must be developed separately under different names. Here's a [tangentially related xkcd](https://xkcd.com/927/) that I can never resist sharing.] Mirroring Nosek, this guide from PayPal has some very helpful and thoughtful advice on the challenges of building and InnerSource culture and the necessary structure for it to succeed in an enterprise setting.

Two ideas of particular interest to me were those of the Trusted Commiter role and of passive documentation. 

The discussion of the Trusted Commiter focuses largely around incentives for internal maintainers. Maintainer burnout is a common phenomenon in open source. In InnerSource, this can be further compounded by traditional performance management structures not being fully prepared to understand and reward the contributions of internal maintainers versus their peers doing glossy new projects. PayPal suggests rotations in and our of these roles at fixed durations.

Passive documentation is another challenge imported from the open source world and exacerbated in the corporate setting. The key question here is how is knowledge from helping a userbase captured over time? In the "wild", we have forums like StackExchange which make past questions easily discoverable. However, InnerSource risks more of this help moving to private messages or the proverbial watercooler. To mitigate this, the book recommends being proactive about using formal channels of communication like Slack.

