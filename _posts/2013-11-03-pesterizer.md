---
layout: post
title: "Pesterizer"
description: ""
category: 
tags: [dev,animation]
git_widget_repo_name: "pesterizer"
---

{% include JB/setup %}

Move your mouse within the box below.  A box trails the mouse.

This script coule be used for a novel call to action in advertisement or promotion websites.

{% include BE/github_widget %}

<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/pesterizer/css/pesterizer.css" media="screen" type="text/css" />
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/pesterizer/css/app.css" media="screen" type="text/css" />
<div class="pesterizerFrame">
    <button class="youCanStillClickOtherThingsWithPesterizer">Hi</button>
</div>
<script> 
	inlineScript.pesterizer = require.config({
		paths: {
	 		'jQuery': '{{ site.JB.WIDGET_PATH }}/pesterizer/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "pesterizer",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/pesterizer/"
    });
	inlineScript.pesterizer(['app']);
</script>