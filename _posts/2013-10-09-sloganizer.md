---
layout: post
title: "Sloganizer"
description: ""
category: 
tags: [dev,animation,requirejs]
---
{% include JB/setup %}

Bellow is the sloganizer.

Its asset repository is located here. [defualt.github.io/sloganizer/](http://defualt.github.io/sloganizer/)

That repository is published with GitHub Pages (gh-pages).

This blog is also published with GitHub (but with Jekyll blog instead).

They share domain.

The sloganizer assets are called into the page with Require JS.
<style type="text/css">
	.sloganizerAppWrapper{
		width:90%;
		margin:0 auto;
		padding:2em;
		background:#eee;
	}
</style>
<div class="sloganizerAppWrapper"> </div>
<script type="text/javascript">
    var require = {
        urlArgs : "bust="+new Date().getTime()
    };
</script>
<script data-main="http://defualt.github.io/sloganizer/main.js" src="http://defualt.github.io/sloganizer/require.js"> </script>
