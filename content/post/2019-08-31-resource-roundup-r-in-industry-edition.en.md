---
title: 'Resource Roundup: R in Industry Edition'
author: Emily Riederer
date: '2019-08-30'
tags:
  - resources
  - rstats
slug: resource-roundup-r-in-industry-edition
---

One of the ways that practices of reproducible research can be brought into industry is through the development of custom R packages and data tools for one's company / organization. Not only can these tools deliver large efficiency gains and standardization, they ideally infuse corporate culture with the shared passion and mission found in open source communities. 

Similar to [my favorite readings on reproducible research], the benefits of internal R packages are a common theme in my [talks](https://emilyriederer.netlify.com/page/talks/) and on my Twitter feed. As seen, for example, in my 10-tweet answer in the following thread. 

<center>
{{< tweet 1130993623548534785 >}}
</center>

This post is a brief annotated bibliography of a few of my favorite "R use / packages in industry" case studies. There are far more great examples than I could ever cover, but the ones I tend to rely upon span a number of different types of organizations, all of whom use R in different and interesting ways and openly share both the benefits and challenges they've found. My summaries are intentionally kept short so that the authors' words speak for themselves. I'll just share a few key takeaways from each and commonalities between them. I encourage everyone to read the full articles:

- [How R Helps AirBnb Make the Most of It's Data](https://peerj.com/preprints/3182/)
- [How the BBC Visual and Data Journalism team works with graphics in R](https://medium.com/bbc-visual-and-data-journalism/how-the-bbc-visual-and-data-journalism-team-works-with-graphics-in-r-ed0b35693535)
- [Building an R Community at the Urban Institute](https://medium.com/@urban_institute/building-an-r-community-at-the-urban-institute-b66739aaaaa7)  

# Highlights

[**How R Helps AirBnb Make the Most of It's Data**](https://peerj.com/preprints/3182/)    
Ricardo Bion, Robert Chang, Jason Goodman

AirBnb's survey of their R usage embodies the numerous benefits of a shared infrastructure and approach to work. They first describe their R usage across a wide range of activities from product analytics, prototyping future apps and data products with Shiny, creating a sustainable enterprise knowledge store with RMarkdown documents^[check out AirBnb's fantastic open source [Knowledge Repository](https://github.com/airbnb/knowledge-repo) for a solution for hosting and browsing past enterprise research findings], and using cutting-edge modeling packages. 

Key to their widespread R adoption is their `Rbnb` package which contains everything from infrastructure utilities and plot themes to statistical tests and imputation methods. In their words:

> The concept is that anytime anyone on the team solves a problem that they think others might encounter, they can generalize their code, include it into Rbnb and now the whole team can access it.

[**How the BBC Visual and Data Journalism team works with graphics in R**](https://medium.com/bbc-visual-and-data-journalism/how-the-bbc-visual-and-data-journalism-team-works-with-graphics-in-r-ed0b35693535)  

This article recounts the BBC Data Journalism team's adoption of `ggplot2` for graphics. The article gives a transparent, detailed look into the methodical process of growing a base of internal users for `ggplot2`, its custom [`bbplot`](https://github.com/bbc/bbplot) package, and its [open-source graphics cookbook](https://bbc.github.io/rcookbook/).

What most stands out to me about the BBC's experience is the conscientious choice to create both a package and a `bookdown` book to solve related yet distinct problems. The scope of `bbplot` is explicitly limited to core plot styling, including routine yet non-trivial tasks like adding the BBC logo to plots. As the authors explain:

> We resisted the temptation to be too prescriptive and coming up with one-size-fits-all solutions for every potential question that was likely to come up when creating graphics... Our goal was for the package to contain only the functions for things you have to do for every graphic, to make the workflow simple, without making it inflexible, as the flexibility is the real benefit of using ggplot2.

This level of flexibility is important to leaving users feeling both empowered and accountable for their output. However, it leaves on the table some additional room for automation and knowledge sharing since many users likely have similar needs and desire similar plot types.

To strike this balance, the `bbplot` package was supplemented by a cookbook to be a living and breathing source of internal knowledge for distinct, specific features or encodings one might wish to include. As the authors describe:

> The idea is that whenever a member of the data team solves a specific problem, like adding curved arrows to a plot or highlighting a single bar in a bar chart, the code is added to the cookbook to save you and colleagues time next time.

I love the idea of developing internal cookbooks for a number of reasons. First of all, it's a flexible solution which is easier to maintain than a package. From the user perspective, it offers support and structure but avoids any black-box feeling; users are encouraged and nearly required to understand and "own" the code they are using. Finally, from a community building perspective, I can imagine it creates a spirit of shared ownership more quickly because submitting a single plot worth of code would be a less intimidating first pull-request than navigating package internals. 

[**Building an R Community at the Urban Institute**](https://medium.com/@urban_institute/building-an-r-community-at-the-urban-institute-b66739aaaaa7)   
Aaron Williams

The Urban Institute has generously open-source a number of their [R packages and tools for plotting, mapping, accessing, and analyzing various types of data](https://github.com/UrbanInstitute?utf8=%E2%9C%93&q=&type=&language=r). Despite their numerous and diverse open-source contribution, the part of their story that most resonated with me was not the tools themselves but the path towards driving adoption. 

The Urban Institute deploys multiple different strategies to support their community including weekly "casual and hands-on" R Lunch Labs to introduce new skills, on-call support, and seed funding (support for junior staff to enhance R infrastructure). These diverse initiatives help to lower the barriers of entry for new programmers or R users by eliminating the risk or sunk cost of feared "failure". As the article describes:

> Having access to a partner for troubleshooting last-second issues reduces the pressure of deadlines and encourages researchers to step out of their comfort zones. In our experience, 80 percent of effort and stress comes from 20 percent of the work. Our goal is to ease the burden of this 20 percent with technical assistance and a little positive reinforcement.

# Common Themes

Above, I just highlighted some of my favorite points from each article. To stay concise, I didn't repeatedly summarize similar points across these articles. However, I do want to take a moment below to highlight a few critical common themes from all three. 

**Automate routine tasks first**

Early wins at all of AirBnb, BBC, and the Urban Institute stem from internal packages that handled some relatively unglamorous tasks like connecting to databases or styling plots. It's important not to overlook these small wins in favor developing fancier or more complex packages. However, these tools are *critical* to adoption. Often, first-mile tasks (e.g. connecting to databases, getting through corporate proxies) or last-mile tasks (e.g. formatting a `ggplot2`) can create barriers to entry so daunting as to dissuade R adoption. Even proficient R users often copy-paste code for these routine tasks which is distracting and inefficient. 

**Think critically about the best type of vehicle for sharing more complex projects**

Similar to the bias for solving complex problems, there's also a bias towards making everything a package. There's something enticing about the completeness of building a package (or Shiny app). A mix of internal satisfaction and external incentives can create a force of gravity pushing employees towards package building. However, other outcomes, such as the BBC's cookbook, can be equally if not more useful. While not demonstrated in these case studies, I have also found RMarkdown templates or clone-able mock analysis repos to be superior outcomes in certain situations.

Ultimately, the choice depends on countless factors including how unique or routine the task / workflow you want to share is, how much time you can invest in ongoing support and maintenance, and what sort of community contributions you hope to receive. For example, the BBC's cookbook idea harkens back also to the concept of "passive documentation" described in PayPal's excellent [ebook on InnerSource](http://innersourcecommons.org/checklist/). Capturing code in a cookbook is a great way to scale transient, in-person user support by simultaneously creating a permanent artifact. 

In light of all these factors, noticing when and where each company *stopped* developing or left further development to the community is instructive. 

**Invest as much in building the community as the tools**

Building data products is (relatively) easy. Building communities is hard. R devtools are excellent, but there's no code profiler to identify why the community is slow to adopt your great innovations and there's no unit testing suite to check before giving a training too hard or too irrelevant to connect. All of AirBnb, the BBC, and the Urban Institute discuss at length how they had to proactively generate demand for their tools by demonstrating the value of a different way of working. Beyond capturing initial interest, all took multi-pronged approaches to cultivating users and future developers. Just like real open-source communities, internal communities need maintainers, sustainers, advocates, evangelists, and champions. If you aren't spending at least as much time on community building as tool building, likely some of your effort is in vain.

# Getting Started

If any of this sounds like something you would like to bring to your organization but you aren't sure where to start, my post on [RMarkdown Driven Development](http://127.0.0.1:7830/post/rmarkdown-driven-development/) describes a method that I have found effective to convert existing notebooks into reusable packages. 

More broadly, I was excited to see that [rstudioconf::2020](https://web.cvent.com/event/36ebe042-0113-44f1-8e36-b9bc5d0733bf/summary) is offering a training course titled "My Organization's First R Package". Consider checking out the conference for this training and surely countless more great examples of R in action at all types of organizations.