---
layout: post
title: "Pesterizer"
description: ""
category: 
tags: [dev,animation]
---
{% include JB/setup %}
{{ page.url }}
{{ page.url }}
{{ page.categories }}
zxcvzxcv
{{ site.JB.WIDGET_PATH }}
asdfqwer

The pesterizer is a an pesterizer.. 


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