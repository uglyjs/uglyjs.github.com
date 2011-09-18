---
title: No xss please
layout: post
author: twalker
---

A validation rule applied to all text inputs, politely protecting against xss attacks.

{% highlight javascript %}
$.validator.addMethod("script", function (value, element) {
	var v = value.toLowerCase();
	if (v.indexOf("<script") >= 0 || v.indexOf("<xss") >= 0) {
		return false;
	} else {
		return true;
	}
}, "Please do not enter JavaScript into this area.");
{% endhighlight %}
