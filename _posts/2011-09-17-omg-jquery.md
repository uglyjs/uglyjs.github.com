---
title: OMG! I can jQuery!
layout: post
author: James
authorurl: http://padolsey.net
---

How many *bad* things can you count?

{% highlight javascript %}
DayTimeStart = parseInt(DayTimeStart.substring(0,2),10);
NightTimeStart = parseInt(NightTimeStart.substring(0,2),10);
var now = new Date();
var nowHour = now.getHours();       
if(nowHour >= DayTimeStart && nowHour < NightTimeStart){
$("body").css("background-color","#27BBBC");
    $("body").css("background-image","url('/library/images/bg_bodyDay.png')");
    $("body").css("background-repeat","repeat-x");
    $("div#main h1").css("background-image","url('" + HeaderDayImage + "')");
} else {
    $("body").css("background-color","#117071");
    $("body").css("background-image","url('/library/images/bg_bodyNight.png')");
    $("body").css("background-repeat","repeat-x");
    $("div#main h1").css("background-image","url('" + HeaderNightImage + "')");
    $("div#footer").css("background-color","#117071");
    $("a#share").css("left","591px");
}
{% endhighlight %}

* Global variables, which would probably be okay if they were constants.
* Non constructor variables starting with capital letters (e.g. `DayTimeStart`).
* Re-querying for `jQuery('body')`. Pointless, wasteful.
* Application of CSS in JS. It depends on the case, but with this example, the JS should apply a class to the body and then the correct styles should be applied in the StyleSheet.
* Usage of the value `"591px"`. It's uncommented and is not in any describtive constant. It's just there, in the code. Some poor developer will come along and ask: Why 591? Why 591? ... why...
