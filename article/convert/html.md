转换为 HTML 文档
====

MdCharm
----

选择 'File', 'Export to...'，勾选 'HTML', 点击 'Browser...' 选择导出目录并输入导出的文件名，点击 'OK'，即可将当前的 Markdown 文档转换为 HTML 文档。

如果不满意 HTML 文档的样式，可以在设置中自定义 CSS。

Pandoc
----

参考 [Installing](http://pandoc.org/installing.html) 安装 Pandoc。

打开命令行，进入文档所在目录：

```
cd /path/to/file/
```

执行下面的命令，将 Markdown 转换为 HTML：

```
pandoc -o hello.html hello.md
```

>默认的转换，只是将 Markdown 内容转换为 HTML 标签，所以只能看到浏览器的默认样式。

可以执行下面的命令，为导出的 HTML 添加自定义样式：

```
pandoc -o hello.html -c style.css hello.md
```

>`style.css` 仍然是以 `<link>` 的方式关联到 HTML 文档中的，所以在发布的时候需要将 CSS 一同发布出去。
