---
layout: post
title: "Using RequireJS for Importing Demo Content From GitHub Pages into Jekyll"
description: ""
category: 
tags: [dev,RequireJS,Jekyll,GitHub Pages,]
---
{% include JB/setup %}

I have a number of Github respositories with demo pages.  I want to integrate those demos within a [Jekyll](http://jekyllbootstrap.com/) blog site.  Jekyll integrates with Github in an interesting way that I want to take advantage of: a Jekyll repository named http://\[username\].github.io, commited to Github will serve that blog at http://[username].github.io

My demo repositories are served with [Github Pages](http://pages.github.com/).  This makes them accessible at http://\[username\].github.io/\[respository name\].

The blog and the demo pages share a domain:

> http://\[username\].github.io --- *(blog)*  
> http://\[username\].github.io/\[respository name\] --- *(demo page)*

(This is really only useful in case I want store static JSON in a demo repository and load it with AJAX into the blog.)

I want to instantiate the demos as widgets within Jekyll.

For each repository, I wrap all the dependencies in a RequireJS modules.  I refactor the script loading for the Github Pages demo page HTML.  So each demo repository Github Pages page loads its standalone demo page with Require.  I make sure each repository has an "app.js" module which handles instantiation config and call.

It's now possible to call each app.js module into Jekyll.  Just put this into a .md or anywhere else in your Jekyll content:

{% highlight html %}
<div id="someHookForYourWidgetSpecifiedInAppDotJs"></div>
<script> 
	var someWidgetNameRequire = require.config({
		paths: {
	 		'jQuery': 'http://ajax.googleapis.com/ajax/libs/jquery/2.0.2/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "someWidgetName",
         baseUrl: "http://defualt.github.io/someWidgetName"
    });
	someWidgetNameRequire(['app']);
</script> 
{% endhighlight %}

To break this down a little:
- "someHookForYourWidgetSpecifiedInAppDotJs" is a div that you use to instantiate your widget.  It's selected and used in your app.js demo-repository file.  An element with this ID should also appear in your Github Pages repository demo page for when you instantiate the widget over there.
- You can see how jQuery is injected as a dependency.  This should match your Github Pages implementation.
- "context" is used to seperate this widget's dependencies from other widgets.
- "baseUrl" is used to retain the widget's module's internal mapping of it's central dependencies.

A drawback of seperating widget contexts from one another is that dependencies that are common among various widgets must load once for each.  I think that Require avoidsd loading the scripts from their servers multiple times.  But there should be a higher memory impact from loading, say, jQuery into multiple contexts.  I need to confirm this about RequireJS.

I also don't think there's any hope using r.js to optimize within Jekyll with all these contexts.

What this accomplishes for me a is simplified workflow for updating my demo Github Pages and automatically seeing those changes in my blog/portfolio.



