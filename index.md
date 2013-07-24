---
layout: page
title: Brian's Brain's Blog
tagline: Making stuff up
---
{% include JB/setup %}

This is the home page in a blog hosted on [GitHub](http://defualt.github.io/).  The blog was created with the [Jekyll](http://jekyllrb.com/) blogging framework, with guidance from [jekyllbootstrap.com](http://jekyllbootstrap.com/).

Jekyll is built on top of the Ruby programming language.  This is the first time I've worked with Ruby.  Jekyll uses Ruby substantially to generate static HTML webpages.

##Why GitHub/Jekyll approach?

- It uses [Markdown](http://daringfireball.net/projects/markdown/) which makes writing and formatting content a breeze.  Another markdown-focused project I'm working on is a markdown-to-pdf/docx/html [resume generator](https://github.com/defualt/resume).

- GitHub hosting is free and fashionable.

- There is no database, which is interesting compared to Wordpress's substantial dependency on databases.

- Jekyll serves static HTML, which is a departure from my dynamic web app framework obsession.  This makes SEO much easier.

##Why this approach sucks

- It doesn't.

- But if it did, it would be because user submitted content is limited.  

- This is because its not hosted on a dynamic web server.

- In order to have discussion threads, my options are limited.
  - I can use an AJAX service like [Disqus](http://disqus.com/).  But this is bad for SEO. 
  - I can use this [hack](http://theshed.hezmatt.org/jekyll-static-comments/), which pipes comments through email.  It's really clever and has some anti-spam utility.  It also preserves SEO.  The problem is that comments do not appear immediately so discussion is lagged.  


