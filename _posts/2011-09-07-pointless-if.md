---
title: Pointless If statement
layout: post
author: James
authorurl: http://padolsey.net
---

We've all seen this:

{% highlight javascript %}
if (kRegex.test(value)) {
    return true;
} else {
    return false;
}
{% endhighlight %}

Eew.

*Beautified*:

{% highlight javascript %}
return kRegex.test(value);
{% endhighlight %}
