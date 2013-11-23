---
layout: post
title: "Grunt Tips"
description: ""
category: 
tags: [grunt]
asdf: "qwer"
---
{% include JB/setup %}

{{ page.asdf }}

### Update packge.json
`npm install grunt-string-replace --save`

### Pass arguments into grunt

`grunt whateverTask --someArg=XYZ`

Inside the Gruntfile.js

'var someVar = grunt.option("someArg");'

