---
layout: post
title: "Accordionizer"
description: ""
category: 
tags: [dev,animation]
git_widget_repo_name: "accordionizer"
---
{% include JB/setup %}

## What is an accordion UI

A Vertical accordion UI (examples) is a column of stacked buttons.  When you click on a button, an content area appears beneath that click button.  As a consequence of this appearance, the buttons beneath the clicked button get offset downward by a distance equal to the appearing content area's height.

(demo of a basic accordion)

## Issues with other vertical accordion UIs

###Usability

There is a usability issue with typical vertcial accordion UI examples.  When you click on a button that is positioned at the bottom of the interface's frame, the content area that is generated is obscured by the bottom of the window frame.

The content area might be partially obscured, or it might be completely obscured.  If it is completely obscured, clicking the button will not yield any visual cue, and it would seem to the user that their button click was completely ineffectual.

The user must compensate for this usability issue by scrolling the content area into view after the content area has appeared.

On the accordion below, click the button named "last."  No visual change.  Now scroll the box to finally find the content.

(make a demo from description above)

###Animation

Accordion interfaces present an opportunity to add animation to your interface.  Most animated HTML/CSS/JS accordion interface solutions neglect to optimize for mobile.  In order to optimize animation for mobile, you need to leverage CSS 3D transforms, and it's difficult to do this in this particular application.

####	The conventional, problematic approach is implimented like this:

You have a stack of buttons.  You click buttonX.  ContentAreaX appears beneath buttonX with a height of 0, positioned relative, and overflow hidden. ContentAreaX has one immediate child element with an innerWrapper class, and within innerWrapper is the rest of the HTML. ContentAreaX animates it's height property higher until it reaches the height of its innerWrapper.  As the height increase, the buttons beneath ContentAreaX are pushed down automatically.

There is no 3D transform property for height.  There is one for scale, but that's not visually equivalent, and it doesn't have the automatic effect of pushing the lower buttons down.

## The Accordionizer solves these issues

- it automatically positions the content for maximal visibility relative to the interface's frame
- it is implemented with CSS 3D transforms for fluid animation on both desktop and mobile.


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