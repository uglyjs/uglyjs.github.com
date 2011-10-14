---
title: Links plus
layout: post
author: Gavin Logan (@tamewhale)
authorurl: http://twitter.com/tamewhale
---

Working on a recent project I kept coming across anchor tags like this:

{% highlight html %}
<a href="#" onclick="visit_url(<?php echo $url; ?>)">
{% endhighlight %}

I was really curious as to what `visit_url()` would do, eventually I found it:

{% highlight javascript %}
function visit_url(url) {
    window.location = url;
}
{% endhighlight %}