转换为 PDF 文档
====

MdCharm
----

与导出 HTML 文档类似，选择 'File', 'Export to...'，勾选 'PDF', 点击 'Browser...' 选择导出目录并输入导出的文件名，点击 'OK'，即可将当前的 Markdown 文档转换为 PDF 文档。

如果不满意 PDF 文档的样式，可以在设置中自定义 CSS。

Pandoc
----

使用 Pandoc 导出 PDF 文档，需要先安装某个 LaTeX 引擎（参考 [Creating a PDF](http://pandoc.org/README.html#creating-a-pdf)）。然后执行命令：

```
pandoc -o hello.pdf hello.md
```

当然，也可以通过 `-c style.css` 来指定样式文件。

Chrome
----

在将 Markdown [转换为 HTML 文档](html.md) 之后，可以通过 [Chrome 浏览器](https://www.google.com/chrome/) 打开它。选择 '打印'（Ctrl+P），然后更改 '目标打印机' 为 '另存为 PDF'，再进行一些设置后，即可保存为 PDF 文档。
