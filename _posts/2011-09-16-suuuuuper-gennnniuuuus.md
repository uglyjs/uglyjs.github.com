---
title: The javascript super genius
layout: post
author: Jon Beebe
authorurl: http://www.somethingkindawierd.com
---
All credit for this code goes to Richard E. Walker. Inside our html code we see 
the following. *Note it's not in a javascript file, but rather the contents are embedded into the html. __Genius!__*

{% highlight javascript %}
    // filename:windows.js
    // javascript lib. for making pop up windows
    // richard e. walker, suuuupppppppppppppppppperrrrrrrrrrrrrr geennnnnnnnnnnnnniuuuuussssssss
{% endhighlight %}

Later we find this comment, also around some embebbed js functions:

{% highlight html %}
    <!--  this is a javascript library...
    filename:javascript.js

     Richard E. Pluribus Unum Walker
     suuuuuuuuuupppperrrrr geeeeeeeeennniuuuuusssss

    -->
{% endhighlight %}

Now that we've established the author as a certifiable genius, what does he have to offer us?

1) Demonstrating the genius' way of padding numbers

{% highlight javascript %}
    function twoPlaces( num )
    {
        if ( num < 10 ) num = '0' + num;
        return num;
    }
{% endhighlight %}

2) Demonstrating the proper use mixing explicit/implied open/close curly brackets. All geniuses will agree this is a best-practice.

{% highlight javascript %}
    function DebugObject(winOUT,debugOBJ) {
    if (! debugOBJ)
            return(false);

    if ( winOUT.document ) {
            var dOUT = winOUT.document;
    } else if (winOUT.contentDocument) {
            var dOUT = winOUT.contentDocument;
    } else {
            alert("cant find browser document");
            return(false);
    } // end if

    ...more of the same mixture ...

    }
{% endhighlight %}

3) Liberal use of tabs when formatting code, creating a zen-like editing experience (on 8-space-tab setups).
Converted to spaces here to ensure proper viewing.

{% highlight javascript %}
function SetStartTimesFunc( myDate )
{
        var wantedTime        =        document.getElementById( 'SetStartTimes' );
        CheckOnTimeInput( wantedTime );
        var inputs        =        document.getElementsByTagName( 'INPUT' );

        for ( var i = 0; i < inputs.length; i++ )
        {
                var thisInput        =        inputs[i];

                parts                =        thisInput.id.split(':');

                if ( parts[0] == 'AuctionStart' )
                {
                        thisInput.value                =        myDate + ' ' + wantedTime.value;
                }
        }
}
{% endhighlight %}

All of this inside a web-app utilizing 5 iframes, cookies, and javascript in a single page to simulate ajax-like behavior.

