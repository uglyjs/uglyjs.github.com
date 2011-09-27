---
title: How NOT to implement styled checkboxes/radio buttons
layout: post
author: David Wosnitza (_druu)
---

While rescuing a project started by a straight-from-university intern, I came across his very [enterprisy](http://enterprise-js.com/) approach on creating nice and fancy styled checkboxes and/or radio buttons...

{% highlight javascript %}
<div id="checkbox_unchecked_s" style="background: url('/./images/stories/checkbox/unchecked.png');display:none;width:31px;height:31px;" onclick="this.style.display = 'none';
    	document.getElementById('checkbox_checked_s').style.display = 'inline-block';
        document.getElementById('checkbox_unchecked_m').style.display = 'inline-block';
        document.getElementById('checkbox_checked_m').style.display = 'none';
        document.getElementById('checkbox_unchecked_l').style.display = 'inline-block';
        document.getElementById('checkbox_checked_l').style.display = 'none';
        document.getElementById('form_groesse').value = 's';"  ></div>
<div id="checkbox_checked_s" style="background: url('/./images/stories/checkbox/checked.png');display:inline-block;width:31px;height:31px;"  ></div>
{% endhighlight %}

Needless to say, this appeared multiple times on the same page... copy&pasted... 
