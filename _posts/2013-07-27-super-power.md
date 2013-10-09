---
layout: post
title: "If I could pick a super power"
description: ""
category: 
tags: []
---
{% include JB/setup %}

It would be the ability to mute other people and other things.  I would blast them with a zone of silence.  They would be unharmed except completely silent to themselves and everybody else until it wears off.  I would be called The Mute.  A savior for some.  A villian to others. zxcv
<script>
	window.onload=function(){
		var $body = $('body');
		$body.append('asdfasdfasdf')
		var $container = $('#sloganizer');
		var deferred = $.getJSON( "sloganizer/build/page.json");
		deferred.success(function(json){
			console.log(json)
			$container.append(json.head)
			$container.append(json.body)
			$container.append(json.scripts)
		})
	}
</script>
<p id="sloganizer">asdfasdfa</p>