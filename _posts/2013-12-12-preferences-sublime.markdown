---
title: Sublime Text 的详细配置
layout: post
createdate: 2013-12-12 11:10:01
guid: 2013121201
description: 最近迷上了一款文本编辑器`Sublime Text`，给人的第一感觉是轻，而且里面的各种自定义配置用起来真的是如鱼得水。但是里面的配置文件有点恼火，然后去搜索了下，具体配置如下`Preferences.sublime`：
tags:  
  - Sublime Text
  - 配置文件
---
最近迷上了一款文本编辑器`Sublime Text`，给人的第一感觉是轻，而且里面的各种自定义配置用起来真的是如鱼得水。
但是里面的配置文件有点恼火，然后去搜索了下，具体配置如下`Preferences.sublime`：
{% highlight Java %}

{
    //主题文件的位置
    "theme": "Centurion.sublime-theme",
    "color_scheme": "Packages/Color Scheme - Default/Monokai.tmTheme",
    //字体
    "font_face": "Consolas",
    //字体大小
    "font_size": 11.0,
    "ignored_packages":
    [
        "Vintage"
    ],
    //每行code相对于上一行代码的上边距
    "line_padding_top": 2,
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