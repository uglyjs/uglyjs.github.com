---
title: When you let PHP generate your Javascript
layout: post
author: George
authorurl: http://audaccon.com
---

{% highlight javascript %}

<script> 
$(document).ready(function(){
    $("#flip1").hover(function(){
        $("#panel1").slideToggle("fast");
    });
});
</script>
<script>
$(document).ready(function(){
    $("#flip2").hover(function(){
        $("#panel2").slideToggle("fast");
    });
});
</script>
<script>
$(document).ready(function(){
    $("#flip3").hover(function(){
        $("#panel3").slideToggle("fast");
    });
});
</script>
<script>
$(document).ready(function(){
    $("#flip4").hover(function(){
        $("#panel4").slideToggle("fast");
    });
});
</script>
<script>
$(document).ready(function(){
    $("#flip5").hover(function(){
        $("#panel5").slideToggle("fast");
    });
});
</script>
<script>
$(document).ready(function(){
    $("#flip6").hover(function(){
        $("#panel6").slideToggle("fast");
    });
});
</script>
<script>
$(document).ready(function(){
    $("#flip7").hover(function(){
        $("#panel7").slideToggle("fast");
    });
});
</script>

{% endhighlight %}

*Beautified*:

Hire someone who knows how to write JS that doesn't write such things
