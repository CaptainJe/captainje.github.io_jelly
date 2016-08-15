---
layout: post
title: MarkDown快速入门
categories: BlogBuild
comments: true
description: 快速浏览MarkDown基本语法
keywords: MarkDown
---
# MarkDown 常用语法快速入门
最近刚刚用Hexo把Blog安家在Github上，之前没用过MarkDown写东西，稍微看下语法和效果就喜欢上这样写东西的感觉。
MarkDown作者的官方链接： http://daringfireball.net/projects/markdown/  
这里应该是最权威标准的语法了，然而还有一些派生的语法比如Github Flavored Markdown，提供更多功能支持：   
https://help.github.com/articles/github-flavored-markdown/
这里总结下写博客经常用到的语法，同时初体验用MarkDown写东西的感觉：  
## **标题**

```
# 1阶标题
## 带下划线的2阶标题
### 3阶标题
#### 4阶标题
##### 5阶标题
###### 6阶标题
```
># 1阶标题
>## 带下划线的2阶标题
### 3阶标题
#### 4阶标题
##### 5阶标题
###### 6阶标题  

## **文本强调**
```
*斜体*
**加粗**
***粗斜体***
```
>*斜体*
**加粗**
***粗斜体***  

这里顺便说下，MarkDown没有设置字体，字号，字体颜色等的语法支持，因为它的设计初衷就是用简单的规则写出漂亮的文章。太关注这些东西反而违背了初衷，如果真的有特殊需求，可以内嵌原生html，比如：  
`<font color="red">Color Font</font>`
><font color="red">Color Font</font>  

另外，标准MarkDown换行是末尾两个以上空格+Enter换行;但Github Flavored Markdwon支持直接Enter换行
```
这是第一行（没空格直接Enter换行）
我换行了么？
这是第一行（末尾加两个空格再Enter换行）  
我换行了么？
```
>这是第一行（没空格直接Enter换行）
我换行了么？
这是第一行（末尾加两个空格再Enter换行）  
我换行了么？

## **下划线**  
```
我是下划线
- - -
我是下划线
***
```

>我是下划线
- - - 
我是下划线
***  


## **引用**

```
>引用了我
还在引用我
仍旧在引用我

不引用了？
```
>引用了我
还在引用我
仍旧在引用我

不引用了？

注意哦：从>开始就一直是引用了，直到换行Enter换一个空行。

## **图片和链接**
```
图片：
![Timo](https://avatars2.githubusercontent.com/u/13464469?v=3&s=460)
连接：
[CaptainJe](http://captainje.github.io/)
http://captainje.github.io/
```
图片：
![Timo](https://avatars2.githubusercontent.com/u/13464469?v=3&s=460)
连接：
[CaptainJe](http://captainje.github.io/)
http://captainje.github.io/

## **列表**
```
* 我是CaptainJe

+ 我是CpatainTimo

- 我是CaptainJe

1. 我是CaptainJe
2. 我是CpatainTimo
3. 我是CaptainTeemo
```
* 我是CaptainJe

+ 我是CpatainTimo

- 我是CaptainJe

1. 我是CaptainJe
2. 我是CpatainTimo
3. 我是CaptainTeemo

## **代码———这几个很好用**

简单的一行代码用\`printf("hello world")`  
>`printf("hello world")`  

多行代码块用\`\`\`+代码高亮风格+代码+\`\`\`最方便：
```C

\```C
printf("hello world");
printf("hello CpatainJe");
printf("hello CaptainTeemo");
```\

```
注意去掉字符“\`\`\`\前面和后面的\”

```C++
printf("hello world");
printf("hello CpatainJe");
printf("hello CaptainTeemo");
```

代码高亮用的是highlight.js。
这里可以查看highlight.js支持的语言：<https://highlightjs.org/static/demo/>

## **插入视频和音乐**
只能嵌入html元素啦，
哈哈，这个是我废了点功夫才找到的方法：
音乐
```
Howl-Florance and the Mchine:
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=2589607&auto=1&height=66"></iframe>

一个随意的歌单：
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=450 src="http://music.163.com/outchain/player?type=0&id=103196406&auto=1&height=430"></iframe>
```
Howl-Florance and the Mchine:
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=2589607&auto=1&height=66"></iframe>

一个随意的歌单：
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=450 src="http://music.163.com/outchain/player?type=0&id=103196406&auto=1&height=430"></iframe>

视频也一样，这些都是外链播放器，感兴趣的可以搜索下优酷外链播放器和网易云音乐外链播放器

## 补充
1. 2015.12.08： 想要在markdown文件中插入空格：输入全角空格，全角空格会被当作中文字符处理，从而保留下来；
