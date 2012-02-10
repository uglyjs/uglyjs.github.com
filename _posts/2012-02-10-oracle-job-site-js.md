---
title: Oracle Job Site JS - a new frontier in ugliness
layout: post
author: Daniel
authorurl: http://dan.cx/
---

One of the many highlights in [oafcoreR121.js](https://irecruitment.oracle.com/OA_HTML/cabo/oajsLibs/oafcoreR121.js):

{% highlight javascript %}
// Used for LOV. Should be removed when we move to new UIX LOV
function lov(a0, a1, a2, a3, a4, a5, a6, a7, a8, a9, a10, a11, a12, a13, a14, c, p)
{
{% endhighlight %}

And who needs CSS classes?

{% highlight javascript %}
function makePressed(el) 
{
  with (el.style) 
  {
    borderLeft = "1px solid #555533";
    borderRight = "1px solid #ffffff";
    borderTop = "1px solid #555533";
    borderBottom = "1px solid #ffffff";
    paddingTop = "2px";
    paddingLeft = "2px";
    paddingBottom = "0px";
    paddingRight = "0px";
  }
}
{% endhighlight %}

{% highlight javascript %}
//bug 9551575:Fix to avoid 'UNDEFINED' message warning box.
if(!message)
{
eval(decodeURI(document.getElementById(closeAnchorId).href));
return;
}
{% endhighlight %}

Thank goodness there's a comment. Without it we might not understand what's going on. Oh wait...

And awesome browser detection:

{% highlight javascript %}
var ie5=document.all&&document.getElementById;
var ns6=document.getElementById&&!document.all;
{% endhighlight %}