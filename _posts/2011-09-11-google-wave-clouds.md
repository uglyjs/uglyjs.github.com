---
layout: post
author: James
author_url: http://padolsey.net
---

Some poor Google employee [had the job](http://wave.google.com/maintenance/index.html) of making a maintenance page for the once-hyped Google Wave. Apparently, we need a function for each cloud, and each wave:

{% highlight javascript %}
var cloudMoved = false;
var cloud2Moved = false;
var cloud3Moved = false;
var WAVE_TIME = 6000;

$(init);

function init()
{
    cloudMove();
    cloud2Move();
    cloud3Move();
    waves2Out();
    waves3Out();
}

function cloudMove()
{
    if (!cloudMoved) {
        $("#cloud").css("left", $("#cloud").offset().left)
    }
    
    $("#cloud").animate(
        //...
    )
}

function cloud2Move()
{
    if (!cloud2Moved) {
        $("#cloud2")
            .css("left", $("#cloud2").offset().left)
    }
    
    $("#cloud2").animate(
        //...
    )
}

function cloud3Move() //... etc.
{% endhighlight %}