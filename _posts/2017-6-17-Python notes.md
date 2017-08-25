---
title: "Self in Python "
tags: python 
---


### why we need self in python
* We can always see self in python source code. 
* The word **self** is not strict. We could replace it with whatever we want.
* self represents the instance of the class.

{% highlight python %}
for instance:  
Class Parent:  
  def pprt(self):  
    print self  
Class Child:  
  def cprt(self):  
    print self  

c = Child() #c is the instance of Child() class
c.cprt()
c.pprt()
p = Parent() # p is the instance of Parent() class
p.pprt()
{% endhighlight %}


we could treat c.cprt() as Child.cprt(c)

[see more](http://python.jobbole.com/81921/)

[or here](https://stackoverflow.com/questions/2709821/what-is-the-purpose-of-self)


