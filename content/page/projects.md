---
title: "Projects"
comments: no
---

<style>
.proj-container {
  display: grid;
  grid-gap: 50px;
  grid-template-columns: auto auto;
}

.proj-logo {
  grid-column: 1;
}
.proj-meta {
  grid-column: 2;
  text-align: center;
}
.proj-desc {
  grid-column: 1 / span 2;
}
</style>

<div class = "proj-container">
  <div class = "proj-logo">
      <img src = "/img/projmgr.png" />
  </div>
  <div class = "proj-meta">
      <strong>projmgr: GitHub-based Project Management in R </strong>
      <br/>
      <a href = "https://emilyriederer.github.io/projmgr/">pkgdown website</a> 
      <br/>
      <a href = "https://github.com/emilyriederer/projmgr">GitHub repository</a>
  </div>
  <div class = "proj-desc">
  
<code>projmgr</code> is an R package which provides an opinionated interface to the GitHub v3 REST API with features focused on improving project management workflows. Many data scientists and software engineers commonly use GitHub for version control, storage, and distribution, and priorities are often motivated by GitHub features and bugs. For these reasons, using GitHub issues and milestones for project management offers numerous benefits over external project management tools like JIRA or Trello.
<p/>
Features include:
<p/>
<ul>
<li> GET-ting and POST-ing issues and milestones to GitHub repositories  </li>
<li> Bulk-uploading GitHub issues and milestones from custom YAML templates </li>
<li> Communicating progress through custom visualizations and HTML/CSS reports </li>
</ul>
<p/>
Please see package website for more details, including detailed walk-throughs of functionality and persona/use-case driven cookbooks.  
  
  </div>
</div>

<p/>
<p/>

<div class = "proj-container">
  <div class = "proj-logo">
      <img src = "/img/rtistic-files/logo.png" />
  </div>
  <div class = "proj-meta">
      <strong>Rtistic: A wireframe R package for hacking ggplot2 and RMarkdown styles</strong>
      <br/>
      <a href = "https://github.com/emilyriederer/Rtistic">GitHub repository</a>
  </div>
  <div class = "proj-desc">
  
<code>Rtistic</code> is a minimal wireframe R package. It is not intended to be installed but rather intended to serve as a starting point for groups (e.g. meet-ups, classrooms, workplaces) to collaboatively build out their own set of <code>ggplot2</code> themes and palettes and various RMarkown styles. 
<p/>
The repository contains many templates, scratchpads, and step-by-step instructions for a variety of styling options. You can also read more about it in <a href = "/post/rtistic-a-package-by-numbers-repo/">this blog post</a>.
  
  </div>
</div>

<p/>
<p/>

<div class = "proj-container">
  <div class = "proj-logo">
      <img width = "120" src = "https://raw.githubusercontent.com/emilyriederer/wigo/master/man/figures/logo.png" />
  </div>
  <div class = "proj-meta">
      <strong>wigo: A knitr engine to help understand what is going on in your RMarkdown environment</strong>
      <br/>
      <a href = "https://github.com/emilyriederer/wigo">GitHub repository</a>
  </div>
  <div class = "proj-desc">
  
<code>wigo</code> is light-weight package that provides an alternative <code>knitr</code> language engine. All RMarkdown code chunks are executed with the standard R engine, but chunk output is replaced by a changelog showing a diff of the environment between chunks. This can help uncover opportunities to consolidate or reorganize an RMarkdown.
  
  </div>
</div>