---
title: 网页开发简单教程之HTML
layout: post
createdate: 2013-12-17 20:37:19
guid: 2013121701
description: html即超文本标记语言。它是标准通用标记语言下的一个应用。“超文本”就是指页面内可以包含图片、链接，甚至音乐、程序等非文字元素。超文本标记语言的结构包括头部分（Head）、和主体部分（Body），其中头部（head）提供关于网页的信息，主体（body）部分提供网页的具体内容。--by百度百科
tags:  
  - HTML
---
####什么是HTML?
`HTML`即`超文本标记语言`,它是标准通用标记语言下的一个应用。  
`超文本`指一个页面内可以包含图片、链接，甚至是音乐、程序等非文字元素。  
`超文本标记语言`的语言结构包括头部分(`Head`)和主体部分(`Body`)，其中头部(`Head`)提供关于网页的信息(包含标题、作者、页面编码等)，主体(`Body`)部分提供网页的具体内容(即所要展示的内容)。  
  
####下面我们来看一个具体的页面，代码如下：
{% highlight html %}
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8"/>
        <title>Hello World</title>
    </head>
    <body>
        大家好，这是我的第一个网页。
    </body>
</html>
{% endhighlight %}
以上代码可直接复制到`helloworld.html`文本文档中，保存，然后就可以用浏览器预览：[效果点这里](http://microsimple.github.io/media/demos/demo.html?s=helloworld "查看我的第一个网页")。  
  
下面我将分别说说以上代码代表的含义：  

####&lt;!DOCTYPE html&gt;
定义了当前文件的文档类型和CSS(层叠样式表)规则。我们在一样的html的文档里添加了不同的&lt;!DOCTYPE&gt; 标签时会出现不同的显示效果。  
&lt;!DOCTYPE&gt; 声明位于文档中的最前面的位置，处于 &lt;html&gt; 标签之前。此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范。    
推荐使用上面代码展示的文档头，这是`HTML5`中的写法。  

####&lt;html&gt;...&lt;/html&gt;: 
此元素可告知浏览器其自身是一个 HTML 文档。  
&lt;html&gt; 与 &lt;/html&gt; 标签限定了文档的开始点和结束点，在它们之间是文档的头部和主体。  

####&lt;head&gt;...&lt;/head&gt;:
&lt;head&gt; 标签用于定义文档的头部，它是所有头部元素的容器。&lt;head&gt; 中的元素可以引用脚本、指示浏览器在哪里找到样式表、提供元信息等等。  
文档的头部描述了文档的各种属性和信息，包括文档的标题、在 Web 中的位置以及和其他文档的关系等。绝大多数文档头部包含的数据都不会真正作为内容显示给读者。  
下面这些标签可用在 head 部分：&lt;base&gt;, &lt;link&gt;, &lt;meta&gt;, &lt;script&gt;, &lt;style&gt;, 以及 &lt;title&gt;。  
&lt;title&gt; 定义文档的标题，它是 head 部分中唯一必需的元素。  

####&lt;meta charset="UTF-8"/&gt;:
META标签是HTML标记HEAD区的一个关键标签，它位于HTML文档的&lt;head&gt;和&lt;title&gt;之间（有些也不是在&lt;head&gt;和&lt;title&gt;之间）。  它提供的信息虽然用户不可见，但却是文档的最基本的元信息。&lg;meta&gt;除了提供文档字符集、使用语言、作者等基本信息外，还涉及对关键词和网页等级的设定。  
这里的`chareset=utf-8`代表的是该文件内容的编码格式为`UTF-8`。  

####&lt;title&gt;hello world&lt;/title&gt;:
&lt;title&gt; 元素可定义文档的标题。  
浏览器会以特殊的方式来使用标题，并且通常把它放置在浏览器窗口的标题栏或状态栏上。同样，当把文档加入用户的链接列表或者收藏夹或书签列表时，标题将成为该文档链接的默认名称。  

####&lt;body&gt;大家好，这是我的第一个网页。&lt;/body&gt;:
&lt;body&gt; 元素定义文档的主体(即要展现的内容)。它包含文档的所有内容（比如文本、超链接、图像、表格和列表等等）。   

(over)  
\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-    
参考资料：    
1.w3cschool：http：//www.w3school.com.cn/html  
2.HTML &lt;!DOCTYPE&gt; 标签学习：http://blog.csdn.net/luxideyao/article/details/17027617  
3.常用的 HTML 头部标签：https://github.com/yisibl/blog/issues/1