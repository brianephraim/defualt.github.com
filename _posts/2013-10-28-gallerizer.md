---
layout: post
title: "Gallerizer"
description: ""
category: 
tags: [dev,animation]
---
{% include JB/setup %}

The gallerizer is a an image gallery.  It has a complex and strange animation for image transitions.

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
         baseUrl: "http://defualt.github.io/gallerizer"
    });
	inlineScript.gallerizer(['app']);
</script>