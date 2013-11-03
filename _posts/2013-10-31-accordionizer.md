---
layout: post
title: "Accordionizer"
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

The accordionizer is a an accordionizer.. 
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/accordionizer/css/accordionizer.css" media="screen" type="text/css" />
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/accordionizer/css/app.css" media="screen" type="text/css" />
<style>
.accordionizerScrollDivDemoWrap{position:relative;top:0;}
	.accordionizerScrollDivDemoWrap ul{
		padding:0;
	}
</style>
<div class="accordionizerScrollDivDemoWrap">
	<div class="topNavAndLogoEtc">Welcome to the smartaccordion page.</div>
	<div class="bottomNavAndCopyrightEtc">Welcome to the smartaccordion page.</div>
	<div class="col1">
		<img src="{{ site.JB.WIDGET_PATH }}/accordionizer/guitarcat.jpg" />
	</div>
	<div class="col2">
		<ul class="accordionSpartacus">
			<li>
				<div class="headlineBlurb">ispum small</div>
				<div class="articleContent small">lorem small</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum med</div>
				<div class="articleContent med">lorem med</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum large</div>
				<div class="articleContent large">lorem large</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum mega</div>
				<div class="articleContent mega">lorem mega</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum small</div>
				<div class="articleContent small">lorem small</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum med</div>
				<div class="articleContent med">lorem med</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum large</div>
				<div class="articleContent large">lorem large</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum mega</div>
				<div class="articleContent mega">lorem mega</div>
			</li>
		</ul>
	</div>
	<div class="col3">3</div>
	<div class="col4">
		<ul class="accordionSeeker">
			<li>
				<div class="headlineBlurb">ispum small</div>
				<div class="articleContent small">lorem small</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum med</div>
				<div class="articleContent med">lorem med</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum large</div>
				<div class="articleContent large">lorem large</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum mega</div>
				<div class="articleContent mega">lorem mega</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum small</div>
				<div class="articleContent small">lorem small</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum med</div>
				<div class="articleContent med">lorem med</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum large</div>
				<div class="articleContent large">lorem large</div>
			</li>
			<li>
				<div class="headlineBlurb">ispum mega</div>
				<div class="articleContent mega">lorem mega</div>
			</li>
		</ul>
	</div>
	<div class="col5">5</div>
</div>
<script> 
	inlineScript.accordionizer = require.config({
		paths: {
	 		'jQuery': '{{ site.JB.WIDGET_PATH }}/accordionizer/jquery.min'
	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "accordionizer",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/accordionizer/"
    });
	inlineScript.accordionizer(['app']);
</script>