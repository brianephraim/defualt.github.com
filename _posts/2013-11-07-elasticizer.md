---
layout: post
title: "Elasticizer"
description: ""
category: 
tags: [dev,animation]
git_widget_repo_name: "elasticizer"
---

{% include JB/setup %}

## Hardware accelerated animation (for Android and iOs) of dynamic values with elastic easing curves
### Insufficient approaches

- settimeout animation  
   - e.g. jQuery.animate
   - no hardware acceleration
   - dynamic values capable
   - elastic easing capable
- CSS transitions
   - hardware acceleration capable
   - dynamic values capable
   - no elastic easing
- requestAnimationFrame
   - hardware acceleration capable
   - dynamic values capable
   - no elastic easing
   - doesn't work on Android
- CSS keyframes
   - hardware acceleration capable
   - no dynamic values
   - elastic easing capable

None of these approaches meet the criteria.  requestAnimationFrame comes close, but it has poor support on Android.

### The Elasticizer solution

There's a trick we can do with CSS keyframes.

When we can define translate3d with percentage.  Like this.

{% highlight css %}
@keyframes percentageMove {
	0% {
		-webkit-transform:translate3d(0%,0,0);
	}
	1% {
		-webkit-transform:translate3d(1%,0,0);
	}
	/* ... */
	100% {
		-webkit-transform:translate3d(100%,0,0);
	}
}

{% endhighlight %}

The percentage here is based the width of the parent.  So if the parent is 60px, and you translate3d(50%,0,0), the element moves right 30px.  

In order to animate an element to a dynamic value, wrap the element in a parent element, and make that parent's width the distance to the dynamic value.  Then apply the percentage move keyframes.

This trick is the key to the elasticizer.







{% include BE/github_widget %}

<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/elasticizer/css/elasticizer.css" media="screen" type="text/css" />
<link rel="stylesheet" href="{{ site.JB.WIDGET_PATH }}/elasticizer/css/app.css" media="screen" type="text/css" />

Click within the grey area below to animate the purple square to move to where you clicked.  It has a bouncy animation.

<div class="elasticizerBlogWidgetWrap widgetWrap">
	<div class="elasticizerWidgetFrame"> </div>
</div>
<script> 
	inlineScript.elasticizer = require.config({
		paths: {
	 		'jQuery': '{{ site.JB.WIDGET_PATH }}/elasticizer/jquery.min',
	 		'Tweenable': '{{ site.JB.WIDGET_PATH }}/elasticizer/shifty.min',
	 		'CSSAnimations': '{{ site.JB.WIDGET_PATH }}/elasticizer/css-animations',

	 	},
	 	shim: {
	        'jQuery': {
	            exports: '$'
	        }
	    },
     	 context: "elasticizer",
         baseUrl: "{{ site.JB.WIDGET_PATH }}/elasticizer/"
    });
	inlineScript.elasticizer(['js/app']);
</script>