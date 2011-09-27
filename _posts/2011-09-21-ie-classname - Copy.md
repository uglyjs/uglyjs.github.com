---
title: changeTheClass, with bonus IE workaround
layout: post
author: James
authorurl: http://padolsey.net
---

I'll let this one speak for itself:

{% highlight javascript %}
function changeTheClass(theElement, theClass)
{
	if(document.getElementById(theElement))
	{
		document.getElementById(theElement).setAttribute('class',theClass);
		document.getElementById(theElement).setAttribute("className",theClass); //IE workaround
	}
}
{% endhighlight %}
