---
title: 为原生JavaScript添加getElementByClass方法
layout: post
createdate: 2013-12-11 13:17:22
guid: 2013121101
tags:  
  - JavaScript
  - Code
---
  今天写了应好朋友需求写了个关于设置文章字体大小(大中小)的 [demo](/media/demos/l-m-s-font-size-demo.html)，一开始脑子秀逗了，居然想用原生的`JavaScript对象.getElementByClass("ClassName")` ，真不知道当时怎么想的，而且还跑到网上去搜索。。。好吧，你们尽情的 bs 吧。
  
  然后自己写了个`getElementByClass`，代码如下：
{% highlight JavaScript %}
document.getElementByClass = function(className) {  
    var el = [],  
    _el = document.getElementsByTagName('*'); 
    for (var i=0; i<_el.length; i++ ) {  
        if (_el[i].className == className ) {  
            el[el.length] = _el[i];  
        }  
    }  
    return el;  
}  
{% endhighlight %}
  使用方法如下：
{% highlight JavaScript %}
var nick = document.getElementByClass("user-nick")[0].innerText;  
{% endhighlight %}
  好吧，写好后，一开始效果挺爽，但是一个 class 里有多个 className 的时候，就会出现问题，我又去搜了下，然后又改了下代码，如下(via:令狐葱)：
{% highlight JavaScript %}
function getElementsByClassName(node,className) {
  if (node.getElementsByClassName) { // use native implementation if available
    return node.getElementsByClassName(className);
  } else {
    return (function getElementsByClass(searchClass,node) {
        if ( node == null )
          node = document;
        var classElements = [],
            els = node.getElementsByTagName("*"),
            elsLen = els.length,
            pattern = new RegExp("(^|\\s)"+searchClass+"(\\s|$)"), i, j;
        for (i = 0, j = 0; i < elsLen; i++) {
          if ( pattern.test(els[i].className) ) {
              classElements[j] = els[i];
              j++;
          }
        }
        return classElements;
    })(classname, node);
  }
}
{% endhighlight %}
使用方法：
{% highlight JavaScript %}
function toggle_visibility(className) {
   var elements = getElementsByClassName(document, className),
       n = elements.length;
   for (var i = 0; i < n; i++) {
     var e = elements[i];
     if(e.style.display == 'block') {
       e.style.display = 'none';
     } else {
       e.style.display = 'block';
     }
  }
}
{% endhighlight %}
  ^_^/，ok，完工~
