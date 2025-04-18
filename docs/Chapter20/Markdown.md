# Markdown

&emsp;&emsp;Markdown是一种可以使用普通文本编辑器编写的标记语言，
通过简单的标记语法，它可以使普通文本内容具有一定的格式。

#### 编写工具推荐

[Typora](https://www.typora.io/)

Typora 是一款支持实时预览的 Markdown 文本编辑器。
它有 OS X、Windows、Linux 三个平台的版本，并且由于仍在测试中，
是完全免费的。

Typora 首先是一个 Markdown 文本编辑器，
它**支持且仅支持** Markdown 语法的文本编辑。
在 Typora 官网 上他们将 Typora 描述为 「A truly minimal markdown editor. 」。


#### 认识Markdown

https://sspai.com/post/36610

#### Markdown常用语法

###### 缩进

一个汉字占两个空格大小，所以使用四个空格就可以达到首行缩进两个汉字的效果。有如下几种方法：


&ensp;&ensp;&#8194;&#8194;一个空格大小的表示：&ensp ; 或 &#8194 ; ，此时只要在相应需要缩进的段落前加上 4个 如上的标记即可，注意要带上分号。


&emsp;&#8195;两个空格的大小表示：&emsp ; 或 &#8195 ; ，同理，使用2个即可缩进2个汉字，**推荐使用该方式**。


&nbsp;&nbsp;&#160;&#160;不换行空格：&nbsp ; 或 & # 160; ，使用4个即可。注意！此时的分号为英文分号，但是不推荐使用此方法，太麻烦！


　　使用全角空格(切换快捷键shift+空格)。然后在全角输入状态下直接使用空格键就ok了。看输入法了我感觉不习惯。

###### 换行

两个回车即可


或者使用< br > (<>里没有空格)

###### 加粗

    **内容**

**内容** 　(*与内容之间没有空格)
###### 倾斜

    *内容*
*内容* 　　 (*与内容之间没有空格)

###### 列表

在Markdown 中我们只需要在文字前加上 - 或 * 即可变为无序列表
有序列表则直接在文字前加1\. 2\. 3\. 符号要和文字之间加上一个字符的空格

````
* 1
* 2
* 3

1. a
2. b
3. c
5. d
````

* 1
* 2
* 3

1. a 
2. b
3. c
5. d


    注意*号和.后要加空格后有空格不然不生效
    
###### 插入图片

    ![title](/path/to/img.jpg)
    
###### 表格
语法如下

| 标题1 | 标题2 | 标题3 |
| ----- | ---- | ---- |
| 文本1 | 文本2 | 文本3 |
| 文本4 | 文本5 | 文本6 |



对其方式

| 左对齐 | 居中 | 右对齐 |
| ----- | :---: | ---: |
| 文本1 | 文本2 | 文本3 |
| 文本4 | 文本5 | 文本6 |

表格内文本

| 左对齐 | 居中 | 右对齐 |
| ------ | :---: | ---: |
| *（斜体）文本1* | **（加粗）文本2**| ~~（删除线）文本3~~ |
| [简书](http://jianshu.com) | $\color{red}{红色字}$ |***（加粗斜体）文本6***|

###### 下载链接

[超链接文字](url)
