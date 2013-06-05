Learning-Markdown (Markdown 入门参考)
===================================

编辑/整理：[LearnShare][learnshare]（学习，分享，进步）
- - -

关于Markdown
---------------

1.[Wiki: Markdown](http://zh.wikipedia.org/wiki/Markdown "Wiki: Markdown")
>Markdown 是一种轻量级标记语言，创始人为 John Gruber 和 Aaron Swartz。它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的 XHTML（或者 HTML）文档”。这种语言吸收了很多在电子邮件中已有的纯文本标记的特性。

2.编写 Markdown 就如同编写纯文本一样简单、纯粹：

+ 它方便修改和发布；
+ 很容易转换为 HTML 代码；
+ 有众多语言及应用的相关扩展；
+ 在 GitHub 等环境中有很好的应用；
+ 是编写文档、记录笔记、撰写文章的合适选择。

3.Markdown 完全兼容 HTML 语法，可以直接在 Markdown 文档中插入 HTML 内容：

<table>
  <tr>
		<td>1</td>
		<td>2</td>
	</tr>
	<tr>
		<td>3</td>
		<td>4</td>
	</tr>
</table>

一、段落与换行
--------------

1.段落的前后必须是空行：

空行指的是行内什么都没有，或者只有空白符（空格或制表符）

相邻两行文本，如果中间没有空行
会显示在一行中（换行符被转换为空格）

2.如果需要在段落内强制加入换行（`<br />`）：

可以在前一行的末尾加入至少两个空格  
然后换行写其它的文字

3.Markdown 中的多数区块都需要在两个空行之间。

二、标题
--------

### 1.Setext 形式

H1
==

H2
---

= 和 - 的数量是没有限制的。通常的做法是使其和标题文本的长度相同，这样看起来比较舒服。

### 2.atx 形式

① 可以用对称的 \# 包括文本：

#H1#

② 也可以只在左边使用 \#：

#H1

##H2

###H3

####H4

#####H5

######H6

③ 成对的 \# 左侧和只在左变使用的 \# 左侧都不可以有任何空白，但其内侧可以使用空白。

 ###左侧使用了空格###

#### 内侧使用了空格

三、引用
--------

>1.引用内容

>2.多行内容
>可以在每行前加入 \>

>2.如果仅在第一行使用 \>，
后面相邻的行即使省略 \>，也会变成引用内容

>3.也可以在引用中
>>使用嵌套的引用

>4.或者在引用中
>使用其他 *Markdown* 语法

四、列表
---------

### 1.无序列表

* 可以使用 \* 作为标记
+ 也可以使用 \+
- 或者 \-

### 2.有序列表

1. 有序列表以数字和 . 开始；
3. 数字的序列并不会影响生成的列表序列；
4. 但仍然推荐按照自然顺序（1.2.3...）编写。

### 3.相关事项

1. 无序列表项的开始是：符号 空格；
2. 有序列表项的开始是：数字 . 空格；
3. 空格至少为一个，多个空格将被解析为一个；
4. 如果仅需要在行前显示数字和 .：

05\. 可以使用：数字 \\. 来取消显示为列表

五、代码区块
------------

1.可以使用缩进来插入代码块：

	<html> // Tab开头
		<title>Markdown</title>
    </html>  // 四个空格开头

代码块前需要有至少一个空行，且每行代码前需要有至少一个 Tab 或四个空格；

2.也可以通过 \`\`，插入行内代码（` 是 Tab 键上边、数字 1 键左侧的那个按键）：

例如 `<title>Markdown</title>`

3.代码块中的文本（包括 Markdown 语法）都会以原格式显示，而特殊字符会被转换为 HTML 实体。

六、分隔线
=======

1.可以在一行中使用三个或更多的 \*、\- 或 \_ 产生分隔线：

***
------
___

2.多个 \* 之间可以有空格（空白符），但不能有其他字符：

*	* *
- - -

七、链接
--------

### 1.行内式

① 普通链接：

[Google](http://www.google.com/)

② 指向本地文件的链接：

[icon.png](./image/icon.png)

③ 包含 title 的链接:

[Google](http://www.google.com/ "Google")

### 2.参考式

参考式链接的写法相当于行内式拆分成两部分，并通过一个 *识别符* 来连接两部分。参考式能尽量保持文章结构的简单，也方便统一管理 URL。

① 首先，定义链接：

[Google][link]

第二个方括号内为链接独有的 *识别符*，可以是字母、数字、空白或标点符号。识别符是 *不区分大小写* 的；

② 然后定义链接内容：

[link]: http://www.google.com/ "Google"

其格式为：[识别符] : 空白符 URL title

其中，URL可以使用 <\> 包括起来，title 可以使用 ""、''、() 包括（考虑到兼容性，建议使用 ""），title 部分也可以换行；

链接内容的定义可以放在同一个文件的 *任意位置*；

③ 也可以省略 *识别符*，使用链接文本作为 *识别符*：

[Google][]
[Google]: http://www.google.com/ "Google"

### 3.自动链接

使用 <\> 包括的 URL 或邮箱地址会被自动转换为超链接：

<http://www.google.com/>

<123@email.com>

该方式适合行内较短的链接，会使用 UR L作为链接文字。邮箱地址会自动编码，以逃避抓取机器人。

八、图片
--------

插入图片的语法和插入超链接的语法基本一致，也分为行内式和参考式两种。

### 1.行内式

直接来看例子：

![GitHub](https://help.github.com/assets/help/footer-logo-56d3698f3654d6403360623c353d37ea.png "GitHub,Social Coding")

方括号中的部分是图片的替代文本，括号中的 title 部分和链接一样，是可选的。

### 2.参考式

直接来看例子：

![GitHub][github]

[github]: https://help.github.com/assets/help/footer-logo-56d3698f3654d6403360623c353d37ea.png "GitHub,Social Coding"

### 3.指定图片的显示大小

目前，Markdown 还不支持指定图片的显示大小，不过可以通过直接插入`<img />`标签来指定相关属性：

<img src="https://help.github.com/assets/help/footer-logo-56d3698f3654d6403360623c353d37ea.png" alt="GitHub" title="GitHub,Social Coding" width="50" height="22" />

九、强调
--------

1.使用 \*\* 或 \_\_ 包括的文本会被转换为`<em></em>`，通常表现为斜体：

这是用来*演示*的_文本_

2.使用 \*\*\*\* 或 \_\_\_\_ 包括的文本会被转换为`<strong></strong>`，通常表现为加粗：

这是用来**演示**的__文本__

3.用来包括文本的 \* 或 \_ 内侧不能有空白，否则 \* 和 \_ 将不会被转换：

这是用来* 演示*的_文本 _

4.如果需要在文本中显示成对的 \* 或 \_，可以在符号前加入 \\ 即可：

这是用来\*演示\*的\_文本\_

5.\*、\*\*、\_ 和 \_\_ 都必须 *成对使用*；

十、反斜线
----------

反斜线用于插入在 Markdown 语法中有特殊作用的字符。

这是用来\*演示\*的\_文本\_

十一、编辑器
------------

### 1.Windows：

① [MarkdownPad][markdownpad]

一个非常优秀的 Markdown 编辑器，提供了多文件编辑、实时预览、自定义样式、文件导出等功能，和 Linux 中的 ReTeX 较为类似，提供了全功能的免费版和具有扩展功能的高级付费版。（这篇文章就是在 MarkdownPad 中完成的，它刚刚更新了 2.0 版本，而且我也基本完成了新版的简体中文翻译工作，估计不久后，大家就可以用上中文版了。）

Update：在 2013-03-11 日，MarkdownPad 2.1.4 的升级中包含了简体中文，参考 [MarkdownPad 2 now speaks Chinese and Portuguese!](http://markdownpad.com/news/2013/new-languages-zh-CH-and-pt-PT/ "News and Updates")。

Update：在 2013-04-18 日，MarkdownPad 2.1.13 的升级中解决了我所提交的 Bug——无法全文渲染。参考 [MarkdownPad 2.1.13 Released](http://markdownpad.com/news/2013/version-2.1.13/ "News and Updates")。

② [Texts][texts]

一个所见即所得的 Markdown 编辑器，不过无法直接编辑 Markdown 文件，只能在 HTML 预览中进行编辑，功能稍差一些，不过可以免费试用。

③ [Markpad][markpad]

一个 Win8 UI 风格的 Markdown 编辑器，提供实时预览和导出导入到博客的功能，但不提供导出到 HTML 文件的功能，不过它是完全免费的。

④[MdCharm][mdcharm]

类似于 MarkdownPad 的 Markdown 编辑器，使用 Qt 开发，支持 Windows 和 Linux 平台，可免费试用，比 MarkdownPad 更加轻巧，比 Retext 更加强大。

### 2.Linux：

① [ReText][retext]

开源的 Markdown 编辑器，功能强大，包含简体中文，Linux 中最好用的 Markdown 编辑器。不过，编辑窗口和预览窗口好像没法同步滚动。

### 3.Mac：

① [Mou][mou]

强大而优秀的 Markdown 编辑器。

② [TextMate][textmate]

### 4.基于 Web：

① [Dillinger][dillinger]

强大的 Web Markdown 编辑器，功能不亚于 MarkdownPad 和 ReTeX，而且支持与 GitHub 和 Dropbox 相连接。

② [Markable][markable]

③ [MaHua][mahua]

### 5.其它：

还有许多其它的软件和平台都有相应的扩展或插件支持，如：

+ Submline Text: [MarkdownEditing][markdown-editing]
+ gedit: [gedit-markdown][gedit-markdown]
+ Eclipse: [Markdown Editor plugin][markdown-editor]
+ IntelliJ IDEA: [idea-markdown][idea-markdown]
+ Wordpress: [WP-Markdown][wp-markdown]

[markdownpad]: http://markdownpad.com/ "MarkdownPad"
[texts]: http://www.texts.io/ "Texts"
[markpad]: http://code52.org/DownmarkerWPF/ "MarkPad"
[mdcharm]: http://www.mdcharm.com/ "MdCharm"
[retext]: http://sourceforge.net/p/retext/home/ReText/ "ReText"
[mou]: http://mouapp.com/ "Mou"
[textmate]: http://macromates.com/ "TextMate"
[dillinger]: http://dillinger.io/ "Dillinger"
[markable]: http://markable.in/editor/ "Markable"
[mahua]: http://mahua.jser.me/ "MaHua"
[markdown-editing]: http://ttscoff.github.com/MarkdownEditing/ "MarkdownEditing"
[gedit-markdown]: http://www.jpfleury.net/en/software/gedit-markdown.php "gedit-markdown"
[markdown-editor]: http://www.winterwell.com/software/markdown-editor.php "Markdown Editor plugin"
[idea-markdown]: http://plugins.jetbrains.com/plugin/?id=5970 "idea-markdown"
[wp-markdown]: http://wordpress.org/extend/plugins/wp-markdown/ "WP-Markdown"

十二、参考资料
--------------

1. [Project Markdown][project-markdown]
2. [Markdown Syntax zh_TW][syntex-tw]
3. [Markdown Syntax CN][syntex-cn]
4. [Wiki Markdown][wiki-markdown]
5. [XBeta Wiki Markdown][xbeta-markdown]

[project-markdown]: http://daringfireball.net/projects/markdown/ "Project Markdown"
[syntex-tw]: https://github.com/othree/markdown-syntax-zhtw/blob/master/syntax.md "Markdown Syntax zh_TW"
[syntex-cn]: http://wowubuntu.com/markdown/ "Markdown Syntax CN"
[wiki-markdown]: http://zh.wikipedia.org/zh-cn/Markdown "Wiki Markdown"
[xbeta-markdown]: http://xbeta.org/wiki/show/Markdown "XBeta Wiki Markdown"

十三、共享协议
--------------

本文由 [LearnShare][learnshare] 整理并在 [CC BY-SA 3.0][CC] 协议下发布，主要为了给自己和各位朋友作为学习 Markdown 的入门及参考资料。

请各位遵循 [Markdown: License][license] 及其它参考文献的共享协议来使用、修改和发布。

[learnshare]: https://github.com/learnshare "LearnShare"
[CC]: http://zh.wikipedia.org/wiki/Wikipedia:CC "Wiki: CC"
[license]: http://daringfireball.net/projects/markdown/license "Markdown: License"
