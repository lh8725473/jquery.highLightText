jquery.highLightText
====================

jquery high light text

一、功能简述

是对HTML页面上的文字内容进行高亮标记，这个可以用在内容搜索上。纯粹的客户端程序，与后台一点瓜葛都没有。
二、如何使用

使用方法是highLightText，具体为：$(选择器). highLightText(String,可选参数)。例如，

$("body").highLightText("世界杯");

表示的含义就是查询并红色高亮标注body标签下的所有的“世界杯”这个关键字，也就是页面下高亮标注所有的“世界杯”文字。又如：

$(".test").highLightText("空姐 凤姐 芙蓉姐",{markColor: "blue"});

则表示class中有test样式的所有标签下的“空姐”，“凤姐”，“芙蓉姐”文字用蓝色高亮标注。
此方法中，有一个参数是必须的，就是你要搜索的关键字字符串（默认状况下，使用空格隔开可表示多个关键字），还有一个可选参数，可自定义一些样式，关键字处理方法，回调函数等，具体参见本文下一部分。

三、一些可选参数

参见下表：

参数 	默认值 	说明

divFlag 	true 	布尔型，true表示对字符串进行多关键字处理，false表示不处理，整个字符串看成1个关键字

divStr 	" " 	字符串，表示分割多个关键字的字符，默认为空格，如果divFlag为false，此参数将失效

markClass 	"" 	代码高亮的class类，默认为没有样式，如果设置样式，将覆盖默认的红色高亮颜色值

markColor 	"red" 	字符串，指高亮文字的颜色值，默认红色。markClass不为空，则此参数失效。

nullReport 	true 	布尔型，表示当搜索结果为空时，是否弹出提示信息。默认弹出。

callback 	return false; 	回调函数，默认无效果。当存在搜索结果时执行。
