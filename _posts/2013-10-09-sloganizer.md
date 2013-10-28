---
layout: post
title: "Sloganizer"
description: ""
category: 
tags: [dev,animation]
---
{% include JB/setup %}

The sloganizer is a javascript class that renders an animated feature component.

It resembles a slot machine.  Load word banks into it and have it generate random sentences.

<style type="text/css">
	.sloganizerAppWrapper{
		width:90%;
		margin:0 auto;
		padding:2em;
		background:#eee;
	}
</style>
<div class="sloganizerAppWrapper"> </div>
<script> 
	inlineScript.sloganizer = require.config({
		paths: {
	 		'jQuery': 'http://ajax.googleapis.com/ajax/libs/jquery/2.0.2/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "sloganizer",
         baseUrl: "http://defualt.github.io/sloganizer"
    });
	inlineScript.sloganizer(['app']);
</script>