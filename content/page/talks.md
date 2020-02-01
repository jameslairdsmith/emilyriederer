---
title: "Tech Talks"
comments: no
---

I really enjoy sharing ideas - whether that be in person, in direct messages, on Twitter threads, etc. Here, I share materials from these talks. Please reach out if you're interested to talk more about any of these topics!

**Do you want to hear about:**

- How to evolve one-time analysis projects into sustainable data products? Then check out [*RMarkdown Driven Development*](#rmddd)
- How corporations and their analysts can benefit from adapting a data science mindset? Then check out [*What's in your Workflow?: Data science workflows for business analysis*](#wiyw)
- A package I developed at work for discounted cashflow valuations analysis? Then check out [*tidycf: Turning business analysis on its head by turning cashflows on their sides*](#tidycf)
- A framework for inner-source tools and culture? Then check out [*Designing empathetic, empowering, and engaging internal tools for analytics*](#deee)

## RMarkdown Driven Development {#rmddd}
[*rstudio::conf, January 2020 in San Francisco, CA*](https://rstudio.com/conference/) 

RMarkdown enables analysts to engage with code interactively, embrace literate programming, and rapidly produce a wide variety of high-quality data
products such as documents, emails, dashboards, and websites. However, RMarkdown is less commonly explored and celebrated for the important role it can play in helping R users grow into developers. In this talk, I will provide an overview of RMarkdown Driven Development: a workflow for converting one-off analysis into a well-engineered and well-designed R package with deep empathy for user needs. We will explore how the methodical incorporation of good coding practices such as modularization and testing naturally evolves a single-file RMarkdown into an R project or package. Along the way, we will discuss big-picture questions like “optimal stopping” (why some data products are better left as single files or projects) and concrete details such as the {here} and {testthat} packages which can provide step-change improvements to project sustainability.

Slides on [Slideshare](https://www.slideshare.net/EmilyRiederer/rmarkdown-driven-development-rstudioconf-2020)

Video coming soon.


## What's in your Workflow?: Data science workflows for business analysis {#wiyw}
[*Domino Data Pop-Up, November 2017 in Chicago, IL*](https://popup.dominodatalab.com/chicago/)

While business analysis rapidly grows more data-driven, the analyst community is slow to adapt the best practices of data science workflows. Many parallels exists between data science “hot topics” (e.g. reproducibility) and business pain points, but these common needs are obscured by the different “languages” of these two communities. The opportunity cost is greatest in heavily regulated industries such as finance and insurance where documentation and compliance are paramount.

Slides on [Slideshare](https://www.slideshare.net/EmilyRiederer/whats-in-your-workflow)  

<p/>

<div style="position:relative; width:80%; height:0px; padding-bottom:56.25%;">
    <iframe style="position:absolute; left:0; top:0; width:100%; height:100%"
        src="https://www.youtube.com/embed/8UDp7h16QsY?rel=0">
    </iframe>
</div>

<p/>

## tidycf: turning business analysis on its side by turning cashflows on their heads {#tidycf}
[*rstudio::conf, January 2018 in San Diego, CA*](https://www.rstudio.com/conference/)   
*Similar talks given at* [*EARL Boston 2017*](https://earlconf.com/2017/boston/), *RLadies Chicago*, *and internal company conferences*  

Statistical computing has revolutionized predictive modeling, but financial modeling lags in innovation. At Capital One, valuations analysis required legacy SAS platforms, obscure data lineage, and cumbersome Excel cashflow statements. This talk describes development of the tidycf R package to reinvent this process as a seamless, end-to-end workflow.

Reimagining cashflow statements as tidy data facilitates a simple, efficient, and transparent workflow while incorporating more statistically rigorous methods. tidycf leverage the full power of R and RStudio – building on top of the tidyverse; reducing complex crunching, wrangling, and visualization to pipeable functions; guiding analysis and documentation with RMarkdown templates; and incorporating features of the latest development version IDE. Altogether, this delivers a good user experience without the overheard of maintaining a custom GUI.

The resulting package goes beyond “getting stuff done”. tidycf also increases quality, reproducibility, and creativity of analysis; ensures consistency and knowledge transfer; reduces the burdens of documentation and regulation; and speeds innovation and time-to-market – all while guiding less-technical analysts through an immersive crash course to R and the tidyverse.

Slides on [Slideshare](https://www.slideshare.net/EmilyRiederer/tidycf-turning-cashflows-on-their-sides-to-turn-analysis-on-its-head)  
Other rstudio::conf talks on the [RStudio website](https://www.rstudio.com/resources/webinars/#rstudioconf2018)

<p/>

<div style="position:relative; width:80%; height:0px; padding-bottom:56.25%;">
    <iframe style="position:absolute; left:0; top:0; width:100%; height:100%"
        src="https://www.youtube.com/embed/T0pp8n-OSqM">
    </iframe>
</div>

<p/>


## Designing Empathetic, Empowering, and Engaging Internal Tools {#deee}
[*International Data Engineering and Science Association (IDEASS) 2018*](https://www.ideassn.org/chicago-2018/)    
[*Strata NYC 2018*](https://conferences.oreilly.com/strata/strata-ny/)

Tech companies place a premium on user experience. However, this laser-focus on users’ needs is too often missing from the design and development of internal analytical tools. This talk will explore what can be learned from open source development and the open science movement about building sustainable, accessible tools to fuel a vibrant “innersource” community.

Based on experience developing internal R packages at Capital One, this talk proposes the analyst-driven development paradigm for tools development. By reframing work from generating analyses to building reproducible analytical pipelines, analysts can efficiently deliver effective prototypes and finished tools as a simple byproduct of business-as-usual work.

More broadly, we will examine why empathy, empowerment, and engagement are the keys to successful open source and innersource projects, and how analyst-driven development deliberately yet seamlessly invokes these concepts into every step of the development process - from toolset curation to community building.

We will share best practices and lessons learned at Capital One - ranging from broad design philosophy to a specific R-based workflows - to motivate analysts to productionalize their analysis, develop better tools, and drive innovation within their own organizations.
