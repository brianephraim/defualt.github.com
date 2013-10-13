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
<link rel="stylesheet" href="gallerizer/css/style.css" media="screen" type="text/css" />
<style type="text/css">
	.gallerizer{width:80%;}
	.gallerizer .slide{width:80%;}
</style>
<div class="catSlides"> </div>
<script>
	var asdf = require.config({
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
	asdf(['app']);
	var qwer = require.config({
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
	qwer(['app']);
	//asdf(['require','sloganizerMain']);
	// asdf(['main']);
	//require(['http://defualt.github.io/gallerizer/main-built.js']);
	//require(['gallerizer']);
	// var qwer = require.config({
	// 	baseUrl: "http://defualt.github.io/sloganizer/"
	// });
	// qwer(['main2']);
</script>
<script>
/*
	var zxcv = require.config({
		paths: {
	 		'gallerizerMain': 'http://defualt.github.io/gallerizer/main',
	 		//'gallerizer': 'http://defualt.github.io/gallerizer/main'
	 	},
     	//context: "asdf",
     	context: "qwer",
        baseUrl: "http://defualt.github.io/gallerizer/"
        // baseUrl: "http://defualt.github.io/gallerizer/"
    });
	//asdf(['sloganizer','gallerizer']);
	zxcv(['require','gallerizerMain']);
	// asdf(['main']);
	//require(['http://defualt.github.io/gallerizer/main-built.js']);
	//require(['gallerizer']);
*/
</script>


