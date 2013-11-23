---
layout: post
title: "Widgetboilerplate"
description: ""
category: 
tags: [dev,animation]
git_widget_repo_name: "widgetboilerplate"
---
{% include JB/setup %}

{% include BE/github_widget %}

<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/accordionizer/css/accordionizer.css" media="screen" type="text/css" />
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/accordionizer/css/app.css" media="screen" type="text/css" />
<style>
.accordionizerScrollDivDemoWrap{position:relative;top:0;}
	.accordionizerScrollDivDemoWrap ul{
		padding:0;
		margin:0;
	}
</style>
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/pesterizer/css/app.css" media="screen" type="text/css" />
<div class="widgetboilerplateWidgetFrame"> </div>
<script> 
	inlineScript.accordionizer = require.config({
		paths: {
	 		'jQuery': '{{ site.JB.WIDGET_PATH }}/widgetboilerplate/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "widgetboilerplate",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/widgetboilerplate/"
    });
	inlineScript.accordionizer(['js/app']);
</script>