---
title: Hating the back button, and exception abuse
layout: post
author: Daniel15
authorurl: http://dan.cx/
---

Saw these snippets on the site of a company that provides "industry leading solutions". Firstly a 
snippet that was in the `<head>` of every page, intentionally breaking the back button:

{% highlight javascript %}
<script>window.history.forward(1);</script>
{% endhighlight %}

And there was also this function which abuses exceptions for control flow (I'm not too sure why):

{% highlight javascript %}
function crossFrameScripting()
{
	// TT#157678 - Prevent Frame usage. (esamson)
	//if (AgentUtils.isIE)
	//{
		try
		{	
			if(self.document.domain.toString() != top.document.domain.toString())
			{
				throw "Access is denied";
			}
		}
		catch(exc) 
		{
			if (top != self)
			{
				top.location=self.location;
			}
		}
	//}
	// /TT#157678 - Prevent Frame usage. (esamson)
}
{% endhighlight %}