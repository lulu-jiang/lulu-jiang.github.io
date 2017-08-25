---
title: "Inheritance "
tags: python 
---


### The order of inheritance
Guess what is the output should be?

{% highlight python %}
# coding=utf-8

"""
多继承的调用顺序
类的 mro()方法可以打印类的继承顺序
"""


class Init(object):
    def __init__(self, value):
        print 'Init init'
        self.val = value
        print 'value:', self.val


class Add2(Init):
    def __init__(self, val):
        super(Add2, self).__init__(val)
        print 'Add2 init'
        self.val += 2
        print 'value:', self.val


class Mul5(Init):
    def __init__(self, val):
        super(Mul5, self).__init__(val)
        print 'Mul5 init'
        self.val *= 5
        print 'value:', self.val


class Pro(Mul5, Add2):
    print 'Pro class init'

    def __init__(self, val):
        super(Pro, self).__init__(val)
        print 'Pro init'

    print 'Pro class init again'


class Inc(Pro):
    print 'inc class init'
    p = super(Pro)
    def __init__(self, val):
        # self.p.__init__(val)
        super(Inc, self).__init__(val)
        print 'Inc init'
        self.val += 1


print Inc.mro(), "\n Inc val: \n", Inc(5).val
{% endhighlight %}


<a href="https://github.com/sevenlulu" target="_blank" class="btn btn-success"><i class="fa fa-github fa-lg"></i> View on GitHub</a>
