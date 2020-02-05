---
layout: post
title : JS中Date对象getYear()的坑
category : JS
tagline: github
tags : [js, github]
---
{% include JB/setup %}

<h3>JS中Date对象getYear()的坑</h3>
    JS中Date对象getYear(）方法和getFullYear()方法区别

    <h5>getYear()</h5>
    使用getYear()函数的本意是获取年份，以2010年为例，如：

    Js代码 
    var nowd = new Date();  
    var yf = nowd.getYear(); 
    
    在IE中是可以正确获取年份：2010，但是在FF等浏览器下则为：110。
    原因则是 在 FF等浏览器内 getYear 返回的是 "当前年份-1900" 的值（即年份基数是1900）
    而IE则是 当today的年份大于等于2000的时，直接将1900加上了，返回的 2010。    

<h5>getFullYear()</h5>
    使用getFullYear()在IE和FF中都可以正确获取年份：2010


## Next Steps

Please take a look at [{{ site.categories.api.first.title }}]({{ BASE_PATH }}{{ site.categories.api.first.url }}) 
or jump right into [Usage]({{ BASE_PATH }}{{ site.categories.usage.first.url }}) if you'd like.