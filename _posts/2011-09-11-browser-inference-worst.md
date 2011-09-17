---
title: Browser Inference at its worst?
layout: post
author: James
authorurl: http://padolsey.net
---

... or rather, feature-based browser detection, from which it is inferred that another feature/quality occurs (in this case, a time zone offset):

{% highlight javascript %}
//remove time zone offset in IE  
if (window.ActiveXObject) {  
    obj[i].created_at = obj[i].created_at.replace(/[+]\d{4}/, "");  
}
{% endhighlight %}

*Window haz property X? Browser must be E. Therefore, E must have unrelated feature Y.*

*Relevant* feature detection would be better:

{% highlight javascript %}
var canParseTimeOffsetWithoutDesignator = !isNaN(
    +new Date('Mon Jan 01 00:00:00 +0000 2000')
);

if (canParseTimeOffsetWithoutDesignator) {
    // ...
}
{% endhighlight %}

*Something I never knew: IE appears to require a timezone designator along with the offset, so `+0000` won't do, but e.g. `GMT+0000` will do fine.*