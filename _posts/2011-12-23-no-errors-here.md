---
title: No errors here
layout: post
author: Daniel15
authorurl: http://dan.cx/
---

{% highlight javascript %}
<script type="text/javascript">
    function handleError() {
        return true;
    }
    window.onerror = handleError;
</script>
<script type="text/javascript" language="javascript">
    function doCallback1(param1, param2, param3) {
        Callback1.Callback(param1, param2, param3);
    }
    function doCallback2(param1, param2, param3) {
        Callback1.Callback(param1, param2, param3);
        Callback2.Callback(param1, param2, param3);
        Callback3.Callback(param1, param2, param3);
    }
    function doCallback3(param1, param2, param3) {
        Callback2.Callback(param1, param2, param3);
        Callback3.Callback(param1, param2, param3);
    }

    function InitLocation(division) {
        clbDivision.Callback(division);
    }
</script>
{% endhighlight %}

I'm not sure what's worse - The fact that all JavaScript errors are silently ignored, doCallback2 
having three callbacks and doCallback3 having two callbacks, or the use of globals (Callback1, 
Callback2, Callback3). The same site had JavaScript functions with names like "foo" and "bar".

As a side note, an interesting oddity in JavaScript: When you return true in the window.onerror 
handler, this prevents the default event handler. This is the opposite to all the other DOM 0 
events (such as onclick), where returning false prevents the default handler.
