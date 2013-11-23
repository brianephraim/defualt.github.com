---
layout: post
title: "Gallerizer"
description: ""
category: 
tags: [dev,animation]
---
{% include JB/setup %}

The gallerizer is a an image gallery.  It has a complex and strange animation for image transitions.
<link rel="stylesheet" href="/gallerizer/css/style.css" media="screen" type="text/css" />
<style type="text/css">
	.gallerizer{width:80%;}
	.gallerizer .slide{width:80%;}
</style>
<div class="catSlides"> </div>
<script> 
	inlineScript.gallerizer = require.config({
		paths: {
	 		'jQuery': 'http://ajax.googleapis.com/ajax/libs/jquery/2.0.2/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "gallerizer",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/gallerizer"
    });
	inlineScript.gallerizer(['app']);
</script>