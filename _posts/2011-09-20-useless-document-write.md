---
title: Useless use of <code>document.write</code>
layout: post
author: Mathias Bynens
authorurl: http://mathiasbynens.be/
---

While reviewing some [enterprise JavaScript](http://enterprise-js.com/) for a client I came across a couple of these inside `if` clauses:

{% highlight javascript %}
document.write("<scr"+"ipt language=javascript>var some_var = 'some value'<" + "/scr"+"ipt>");
{% endhighlight %}

There’s definitely some room for improvement here. For one, the `language` attribute on the `<script>` element is obsolete in HTML; it can safely be omitted.

{% highlight javascript %}
document.write("<scr"+"ipt>var some_var = 'some value'<" + "/scr"+"ipt>");
{% endhighlight %}

Next, there’s no need to concatenate the string like that — you can just write it out all at once, as long as you [escape the `</script>` end tag](http://mathiasbynens.be/notes/etago "Technically, this isn’t needed if you’re certain the JavaScript will never be used inline in the HTML."):

{% highlight javascript %}
document.write("<script>var some_var = 'some value'<\/script>");
{% endhighlight %}

There are only few good reasons to ever use `document.write`. Writing out `<script>` elements _can_ be one of them, but in this case? Not so much. Believe it or not, the intention of this code snippet was to **create a global variable**. (Polluting the global scope with variables is something that should be avoided whenever possible; however, in this case, the variable really needed to be global.)

Of course, there’s a better way to do that in client-side JavaScript:

{% highlight javascript %}
window.some_var = 'some value';
{% endhighlight %}