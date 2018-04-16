---
layout: single
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/img/stanford-hills-big.jpg
title:  "String Comparison in java"
date:   2017-07-09 02:54:58 +0100
categories: programming java
excerpt: Java string comparison involves a bit more than "normal" comparison operation. The syntax makes sense when you think of it retrospectively
---
Studying computer programming is an amazing skill set. Especially in this era of technology and all that. I mean, having these skills does open a whole new vista of possibilities. Lately I have been doing loads of studying. Taking on several languages at the same time. Although many advice against it, and I am aware of the dangers of combining two or more languages with several syntaxes together, due to the risk of mixing up parts of either of them.

Regardless, I wanted to sort of fast track my learning curve in order to maximize opportunities that may be available in the near future, hence my stance on combining several languages together.

I had previously been majoring in javascript and I really love the language and its potential application across several spheres. However, I recently decided to scratch the surface of Java after having a brief foray into the world of android development.

I have heard it been said that _"the difference between Java and Javascript is like night and day"_, well that's not entirely true. In my recent study I have found that Javascript was sort of based off of Java.

Agreed the syntaxing is vastly different in many ways. One such regard is the fact that Java is a strongly typed language while Javascript is not. What this means is that in Java you must declare the data type for every kind of item you intend to store be it the primitive data types like `integers`, `floats` or Objects like Strings and arrays.

Hence the while the below line of code is perfect in Javascript, it is entirely unacceptable in java:

{% highlight javascript %}
var myString = "a javascript style string declaration";
var number = 35;
{% endhighlight %}

The above sample lines of code can be written in Java as:

{% highlight java %}
String myString = "a Java style string declaration";
int number = 35;
{% endhighlight %}    

That being said many things in Java have to be explitely done. For instance comparing strings in javascript seems a bit more straight forward. In fact it is as straight forward as :

{% highlight javascript linenos %}
var str1 = "This is the first string";
var str2 = "This is the second string";
var str3 = str2;
if(str3 == str2) { //compare str3 and str2
    //print to the console the result
    console.log(true); 
} else { 
    console.log(false);
}
if(str3 == str1) { //compare str3 and str1
    //print to the console the result
    console.log(true);
} else {
    console.log(false);
}
{% endhighlight %}

This would absolutely not work as expected in Java. Java instead has an inbuilt string method, the `equals()` method which you can use to compare strings. It returns a boolean `true` if the compared strings are equals or `false` if otherwise. Hence the above can be expressed in java as:

{% highlight java linenos %}
String str1 = "This is the first string";
String str2 = "This is the second string";
String str3 = new String(str2);
if(str3.equals(str2)) { //compare str3 and str2
    //print to the console the result
    System.out.println(true)
} else { 
    System.out.println(false);
}
if(str3.equals(str1)) { //compare str3 and str1
    //print to the console the result
    System.out.println(true)
} else { 
    System.out.println(false);
}
{% endhighlight %}

Although using the `==` comparison operator in Java won't return an error, it just wouldn't work as intended. This is because applying the `==` to two String references simply determines whether or not both references refer to the same object. And as in out example above they don't since we made `str3` refer to an entirely differnt object by using the `new` keyword in its declaration in line 3:

The case would have been slightly different had we instead just used the assignment operator without the `new` keyword as below. Then both `str3` and  `str2` would refer to the same object. 
{% highlight java %}
String str3 = str2;
{% endhighlight %}

In the above case the `==` comparison operator can be used. As can be seen the limitation of this is its lack of robustness. Hence the need and usefulness of the `.equals()` String method.

I'd be glad to review any concept you might be having an issue with just leave me a comment below. Thanks for reading!!!