---
title: Sublime Text 的详细配置
layout: post
createdate: 2013-12-12 11:10:01
guid: 2013121201
description: 最近迷上了一款文本编辑器`Sublime Text`，给人的第一感觉是轻，而且里面的各种自定义配置用起来真的是如鱼得水。写这篇文章主要是做个备份。
tags:  
  - Sublime Text
  - 配置文件
---
最近迷上了一款文本编辑器`Sublime Text`，[官网](http://www.sublimetext.com/ "Sublime Text 官网")，给人的第一感觉是轻，而且里面的各种自定义配置用起来真的是如鱼得水。写这篇文章主要是做个备份。

安装`Package Control`首先打开`Console`，快捷键：`Ctrl+Esc下面的那个键`，输入如下代码，然后回车(`Sublime Text3 `)
{% highlight python %}
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
{% endhighlight %}

`Sublime Text 2`代码如下：
{% highlight python %}
import urllib2,os; pf='Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler( ))); open( os.path.join( ipp, pf), 'wb' ).write( urllib2.urlopen( 'http://sublime.wbond.net/' +pf.replace( ' ','%20' )).read()); print( 'Please restart Sublime Text to finish installation')
{% endhighlight %}

重启软件后，快捷键`Ctrl+Shift+P`就可以打开`Package Control`了，可以在里面安装很多相应的插件。
接下来就是菜单栏`Preferences>Setting User`配置文件，去搜索了下，具体配置如下`Preferences.sublime`:
{% highlight java %}
{
    //主题文件的位置
    "theme":"Centurion.sublime-theme",
    "color_scheme":"Packages/Color Scheme - Default/Monokai.tmTheme",
    //字体
    "font_face":"Consolas",
    //字体大小
    "font_size":11.0,
    "ignored_packages":
    [
        "Vintage"
    ],
    //每行code相对于上一行代码的上边距
    "line_padding_top":2,
    //tab键缩进用空格代替
    "translate_tabs_to_spaces":true,
    //tab键制表符宽度
    "tab_size":4,
    //是否显示行号
    "line_number":true,
    //是否显示代码折叠按钮
    "fold_buttons":true,
    //不管鼠标在不在行号边栏，代码折叠按钮一直显示
    "fade_fold_buttons":true,
    //按回车时，自动与制表位对其
    "auto_indent":true,
    //自动匹配引号，括号等
    "auto_match_enabled":true,
    //突出显示当前光标所在行
    "highlight_line":true,
    //设置光标闪动方式
    "caret_style":"smooth",
    //是否特殊显示当前光标所在的括号、代码头尾闭合标记
    "match_brackets":true,
    //切换到其他文件标签或点击其他非本软件区域，文件自动保存
    "save_on_focus_last":true,
    //代码提示
    "auto_complete":true,
    //设置为true时，按Tab会根据前后环境进行代码自动匹配补全
    "tab_completion":true,
    //选中的文本按Ctrl+F时，自动复制到查找面板的文本框里
    "find_selected_text":true
}
{% endhighlight %}