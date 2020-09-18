#Markdown 简明语法

##区块元素

###段落和换行
段落前后要有一个以上的空行，单纯的回车空行在markdown中是不可行的，添加空行或回车，应当在插入处先按入两个以上的空格然后回车。 
 
###标题
Markdown支持两种标题的语法，类*Setext*和类*atx*形式。
> 类*Setext*形式是用底线的形式，利用`=`(最高阶标题）和`-`(第二阶标题),例如:  
This is an H1 .  
==============  
This is an H2 .
--------------  
可以是任何数量的`=`和`-`。  
  
> 类*Atx*形式是在行首插入1到6个`#`,对应标题的1到6阶，例如：
# 这是H1
### 这是H3
###### 这是H6  
  
###区块引用Blockquotes
Markdown标记区块引用是使用类似email中用`>`的引用方式，如：
> This is a blockquote with two paragraphs. 
> 
> Donec sit amet nisl.  
也可以在整个段落的第一行最前面加一个`>`。同时区块引用是可以嵌套的，区块内可以使用Markdown的语法。  
  
###列表
Markdown支持有序列表和无序列表。  
无序列表使用星号、加号或是减号作为列表标记：
> * red
> * green
> * blue  
> 等同于 :
> + red
> + green
> - blue  
  
有序列表则使用数字接着一个英文句点：
> 1. Bird
> 2. McHale
> 3. Parish  

行首出现‘数字-句点-空白’，如果要避免，可以在句点前面加上`\`。 
 
###代码区块
Markdown中建立代码区块，需要缩进4个空格或是一个制表符，例如：  
	
	<?php
			$a = 1 ;
			$b = 2 ;
	?>

###分隔线
可以使用三个以上的星号、减号、底线来建立分隔线，行内不能有其他东西，也可以在星号或者减号中间插入空格，如下：
> * * *
> * * * *
> - - -
> ___

***

##区段元素

###链接
Markdown支持两种形式的链接语法：**行内式**和**参考式**两种形式，两种链接文字都用[方括号]来标记。  
行内式：
> [Baidu](https://www.baidu.com) 这是一个百度的链接。  
> 这还可以使用相对路径，如[ChatRoom](/Users/yuhari/study/chatRoom/client.html)。  
  
参考式，是在链接文字后面再接上另一个方括号，用以填入辨识链接的标记：
> This is [an example] [id] reference-style link .  

接着，在文件任意处，将这个标记的链接内容定义出来,定义不能放在引用之中：
[id]: http://example.com/ "optional Title Here"
*隐式链接标记*功能可以省略指定的链接标记，这时，链接标记被视为链接文字，如：
> [Google][] , a search engine.
[Google]: http://www.google.com 'Google' 
 
###强调
Markdown使用`*`和底线`_`作为标记强调字词的符号，单个会转成斜体，两个则是加粗，如下：
> *one* **one** _two_ __two__
同样，如果插入普通的星号或底线，可以使用反斜线。  

###代码
标记一小段行内代码，可以使用反引号(`` ` ``)将其包起来，如：
> Use the `printf()` function .  
> Please don't use `<blink>` tags.

如果要在代码区段内插入反引号，可以用多个反引号来开启和结束代码区段：
> ``There is a literal backtick (`) here. ``  

###图片
Markdown 使用类似链接的语法来标记图片，同样也有两种样式：**行内式**和**参考式**。  
**行内式**的图片语法看起来是：
> ![Alt text](/path/to/img.jpg "Optional title")

**参考式**的图片语法为：
> ![Alt text][id]  
[id]: url/to/image "Optional title attribute"  

目前无法指定图片的宽高，因此如果有必要，使用<img>标签。  
* * *

##其它

###自动链接
Markdown 支持简短的自动链接的形式处理网址和电子邮件信箱，通过方括号(`<>`)包起来，如：
> <http://www.baidu.com>  
> <yuhari@126.com>

