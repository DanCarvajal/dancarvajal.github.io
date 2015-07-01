---
layout: post
title: Duct Tape a Site Together
---
###Testing the text

Let's test this link [title](http://)

{% highlight html %}
<link rel="stylesheet" href="{{ "/css/main.css" | prepend: site.baseurl }}">
<link rel="canonical" href="{{ page.url | replace:'index.html','' | prepend: site.baseurl | prepend: site.url }}">
<link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css">
<link href='http://fonts.googleapis.com/css?family=Quattrocento|Oswald:400,300' rel='stylesheet' type='text/css'>
</head>
<p> this is a test </p>

{% endhighlight %}
