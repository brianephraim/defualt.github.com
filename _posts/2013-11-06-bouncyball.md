---
layout: post
title: "Bouncyball"
description: ""
category: 
tags: [dev,animation]
git_widget_repo_name: "bouncyball"
---

{% include JB/setup %}

A bouncy ball.

{% include BE/github_widget %}

<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/bouncyball/css/bouncyball.css" media="screen" type="text/css" />
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/bouncyball/css/app.css" media="screen" type="text/css" />
<style>
	.bouncyballWidgetFrame{height:200px;background:pink;}
</style>
<div class="bouncyballWidgetFrame">
    <div class="stage">
        <div class="actor"> </div>
    </div>
</div>
<script> 
	inlineScript.bouncyball = require.config({
		paths: {
	 		'jQuery': '{{ site.JB.WIDGET_PATH }}/bouncyball/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "bouncyball",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/bouncyball/"
    });
	inlineScript.bouncyball(['js/app']);
</script>