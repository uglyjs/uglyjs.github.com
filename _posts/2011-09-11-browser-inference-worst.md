---
layout: post
author: James
authorurl: http://padolsey.net
---

Browser inference at its worst?

{% highlight javascript %}
//remove time zone offset in IE  
if (window.ActiveXObject) {  
    obj[i].created_at = obj[i].created_at.replace(/[+]\d{4}/, "");  
}
{% endhighlight %}