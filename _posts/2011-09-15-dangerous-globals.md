---

title: Dangerous globals

layout: post

author: Julien

---


This is a common, maybe the first, bad practice but some people are really not afraid about using a lot of globals. IKEA's devs are those kind of guys. No litterals, no namespace, no scope, it works today, why would it fail tomorrow ?

{% highlight javascript %}

<script type="text/javascript" language="JavaScript">
[…]
var width = "Width:";
var height = "Height:";
var length = "Length:"
var cm = "cm";
var kg = "kg";
[…]
{% endhighlight %}

This code is from any product page, look at [this page](http://www.ikea.com/us/en/catalog/products/10159834) for instance, from line 983.