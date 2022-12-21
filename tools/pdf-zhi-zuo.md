# PDF 制作

## wkhtmltopdf

* [wkhtmltopdf downloads](https://wkhtmltopdf.org/downloads.html)

命令格式： `wkhtmltopdf [GLOBAL OPTION]... [OBJECT]... <output file>`

1. 信息 `wkhtmltopdf -V`
2. 把一个html文件转换成PDF `wkhtmltopdf xxx.html xxx.pdf`
3. 把一个 url 指向的网页转换成PDF `wkhtmltopdf url xxx.pdf`
4. 把html文件 和 url指向的网页 转换成图片
   * `wkhtmltoimage xxx.html xxx.jpg`
   * `wkhtmltoimage url xxx.jpg`

```
wkhtmltopdf --header-left "some info" --header-right "[date] [time]" --header-line --header-spacing 3 --footer-spacing 3 --footer-center "- 第 [page] 页-" cover cover.url toc --toc-header-text "目录" --disable-dotted-lines xxx.url xxx.pdf
```

### 安装配置路径

`wkhtmltopdf --footer-line --footer-center [webpage]/[page]/[topage]/[date] url XXX.pdf`

其中 webpage 是文件名，page是当前页码，topage是总页码，date是日期

命令格式：`wkhtmltopdf [OPTIONS]… [More input files]`

### 常规选项

* `–allow` 允许加载从指定的文件夹中的文件或文件（可重复）
* `–book*` 设置一会打印一本书的时候，通常设置的选项
* `–collate` 打印多份副本时整理
* `–cookie` 设置一个额外的cookie（可重复）
* `–cookie-jar` 读取和写入的Cookie，并在提供的cookie jar文件
* `–copies` 复印打印成pdf文件数（默认为1）
* `–cover*` 使用HTML文件作为封面。它会带页眉和页脚的TOC之前插入
* `–custom-header` 设置一个附加的HTTP头（可重复）
* `–debug-javascript` 显示的javascript调试输出
* `–default-header*` 添加一个缺省的头部，与页面的左边的名称，页面数到右边，例如： `--header-left '[webpage]' --header-right '[page]/[toPage]' --header-line`
* `–disable-external-links*` 禁止生成链接到远程网页
* `–disable-internal-links*` 禁止使用本地链接
* `–disable-javascript` 禁止让网页执行JavaScript
* `–disable-pdf-compression*` 禁止在PDF对象使用无损压缩
* `–disable-smart-shrinking*` 禁止使用WebKit的智能战略收缩，使像素/ DPI比没有不变
* `–disallow-local-file-access` 禁止允许转换的本地文件读取其他本地文件，除非explecitily允许用 --allow
* `–dpi` 显式更改DPI（这对基于X11的系统没有任何影响）
* `–enable-plugins` 启用已安装的插件 (如Flash)
* `–encoding` 设置默认的文字编码
* `–extended-help` 显示更广泛的帮助，详细介绍了不常见的命令开关
* `–forms*` 打开HTML表单字段转换为PDF表单域
* `–grayscale` PDF格式将在灰阶产生
* `–help` Display help
* `–htmldoc` 输出程序HTML帮助
* `–ignore-load-errors` 忽略claimes加载过程中已经遇到了一个错误页面
* `–lowquality` 产生低品质的PDF/ PS。有用缩小结果文档的空间
* `–manpage` 输出程序手册页
* `–margin-bottom` 设置页面下边距 (default 10mm)
* `–margin-left` 将左边页边距 (default 10mm)
* `–margin-right` 设置页面右边距 (default 10mm)
* `–margin-top` 设置页面上边距 (default 10mm)
* `–minimum-font-size` 最小字体大小 (default 5)
* `–no-background` 不打印背景
* `–orientation` 设置方向为横向或纵向
* `–page-height` 页面高度 (default unit millimeter)
* `–page-offset*` 设置起始页码 (default 1)
* `–page-size` 设置纸张大小: A4, Letter, etc.
* `–page-width` 页面宽度 (default unit millimeter)
* `–password` HTTP验证密码
* `–post` Add an additional post field (repeatable)
* `–post-file` Post an aditional file (repeatable)
* `–print-media-type*` 使用的打印介质类型，而不是屏幕
* `–proxy` 使用代理
* `–quiet` Be less verbose
* `–read-args-from-stdin` 读取标准输入的命令行参数
* `–readme` 输出程序自述
* `–redirect-delay` 等待几毫秒为JS-重定向(default 200)
* `–replace*` 替换名称,值的页眉和页脚（可重复）
* `–stop-slow-scripts` 停止运行缓慢的JavaScripts
* `–title` 生成的PDF文件的标题（第一个文档的标题使用，如果没有指定）
* `–toc*` 插入的内容的表中的文件的开头
* `–use-xserver*` 使用X服务器（一些插件和其他的东西没有X11可能无法正常工作）
* `–user-style-sheet` 指定用户的样式表，加载在每一页中
* `–username` HTTP认证的用户名
* `–version` 输出版本信息退出
* `–zoom` 使用这个缩放因子 (default 1)

### 页眉和页脚选项

* `–header-center*` (设置在中心位置的页眉内容)
* `–header-font-name*` (default Arial) (设置页眉的字体名称)
* `–header-font-size*` (设置页眉的字体大小)
* `–header-html*` (添加一个HTML页眉,后面是网址)
* `–header-left*` (左对齐的页眉文本)
* `–header-line*` (显示一条线在页眉下)
* `–header-right*` (右对齐页眉文本)
* `–header-spacing*` (设置页眉和内容的距离,默认0)
* `–footer-center*` (设置在中心位置的页脚内容)
* `–footer-font-name*` (设置页脚的字体名称)
* `–footer-font-size*` (设置页脚的字体大小default 11)
* `–footer-html*` (添加一个HTML页脚,后面是网址)
* `–footer-left*` (左对齐的页脚文本)
* `–footer-line*` 显示一条线在页脚内容上)
* `–footer-right*` (右对齐页脚文本)
* `–footer-spacing*` (设置页脚和内容的距离)

example `./wkhtmltopdf --footer-right [page]/[topage] http://www.baidu.com baidu.pdf`

`./wkhtmltopdf --header-center ‘报表’ --header-line --margin-top 2cm --header-line url xxx.pdf`

### 表内容选项中

* `–toc-depth*` Set the depth of the toc (default 3)
* `–toc-disable-back-links*` Do not link from section header to toc
* `–toc-disable-links*` Do not link from toc to sections
* `–toc-font-name*` Set the font used for the toc (default Arial)
* `–toc-header-font-name*` The font of the toc header (if unset use --toc-font-name)
* `–toc-header-font-size*` The font size of the toc header (default 15)
* `–toc-header-text*` The header text of the toc (default Table Of Contents)
* `–toc-l1-font-size*` Set the font size on level 1 of the toc (default 12)
* `–toc-l1-indentation*` Set indentation on level 1 of the toc (default 0)
* `–toc-l2-font-size*` Set the font size on level 2 of the toc (default 10)
* `–toc-l2-indentation*` Set indentation on level 2 of the toc (default 20)
* `–toc-l3-font-size*` Set the font size on level 3 of the toc (default 8)
* `–toc-l3-indentation*` Set indentation on level 3 of the toc (default 40)
* `–toc-l4-font-size*` Set the font size on level 4 of the toc (default 6)
* `–toc-l4-indentation*` Set indentation on level 4 of the toc (default 60)
* `–toc-l5-font-size*` Set the font size on level 5 of the toc (default 4)
* `–toc-l5-indentation*` Set indentation on level 5 of the toc (default 80)
* `–toc-l6-font-size*` Set the font size on level 6 of the toc (default 2)
* `–toc-l6-indentation*` Set indentation on level 6 of the toc (default 100)
* `–toc-l7-font-size*` Set the font size on level 7 of the toc (default 0)
* `–toc-l7-indentation*` Set indentation on level 7 of the toc (default 120)
* `–toc-no-dots*` Do not use dots, in the toc

### 轮廓选项

* `–dump-outline` 转储目录到一个文件
* `–outline` 显示目录(文章中h1,h2来定)
* `–outline-depth` 设置目录的深度（默认为4）

### 页脚和页眉

* `[page]` 由当前正在打印的页的数目代替
* `[frompage]` 由要打印的第一页的数量取代
* `[topage]` 由最后一页要打印的数量取代
* `[webpage]` 通过正在打印的页面的URL替换
* `[section]` 由当前节的名称替换
* `[subsection]` 由当前小节的名称替换
* `[date]` 由当前日期系统的本地格式取代
* `[time]` 由当前时间，系统的本地格式取代

`./wkhtmltopdf --footer-right '[page]/[topage]' http://www.baidu.com baidu.pdf`

`./wkhtmltopdf --header-center '报表' --outline --header-line --margin-top 2cm --header-line http://www.hao123.com/ hao123.pdf`

`./wkhtmltopdf --header-left '[webpage]' --footer-center '测试([page]/[toPage])' http://www.baidu.com baidu.pdf`

PDFtk Server Examples

pdf 合并

https://www.pdflabs.com/docs/pdftk-cli-examples/

`wkhtmltopdf --page-size A6 --margin-left 2 --margin-right 2 --enable-local-file-access --header-left "Notes" --header-right "[date] [time] A6 " --header-line --header-spacing 2 --footer-spacing 2 --footer-center "- 第 [page] 页-" toc --toc-header-text "目录" url xxx.pdf`

`wkhtmltopdf --page-width 80 --page-height 120 --margin-left 0 --margin-right 0 --enable-local-file-access --header-left "Notes" --header-right "[date] [time] Kindle " --header-line --header-spacing 2 --footer-spacing 2 --footer-center "- 第 [page] 页-" toc --toc-header-text "目录" url xxx.pdf`

`wkhtmltopdf --page-width 148 --page-height 210 --margin-left 2 --margin-right 2 --enable-local-file-access --header-left "Notes" --header-right "[date] [time] Kindle " --header-line --header-spacing 2 --footer-spacing 2 --footer-center "- 第 [page] 页-" toc --toc-header-text "目录" url xxx.pdf`



`wkhtmltopdf --page-size A6 --margin-left 2 --margin-right 2 --enable-local-file-access --header-left " Notes | Kindle" --header-right "[section] " -–header-font-size 6 --header-font-name "Consolas" --header-line --header-spacing 2 --footer-spacing 2 --footer-center "- [page] of [topage] -" --footer-right "[date] [time] " --footer-font-size 6 toc --toc-header-text "目录" url xxx.pdf`

### 格式调整

1、页面的布局主要是table布局在pdf中可能会切断的问题，解决方法：

```html
tr{page-break-inside: avoid;}
```

2、利用 page-break-before: left; 让以下三个

将会在生成的pdf中都新开一页。

```html
<div class="page1" style="page-break-before: left;"></div>

<div class="page2" style="page-break-before: left;"></div>

<div class="page3" style="page-break-before: left;"></div>
```

3、pdf中还加上了水印，貌似wkhtmltopdf不提供水印方法

切一张水印的图片，比如下面这个：

然后加在这个网页的最外层的父元素上作为背景，然后repeat这个背景，比如：

```html
<div style="background-image: url('https://backimg.png');background-size: 300px;">

    //网页内容

    //网页内容

    //网页内容

</div>
```

最后实现了水印的效果，需要提醒一下的是，做水印的时候有可能我们网页的效果和pdf的效果有差距，我调试的时候是遇到了，明明网页上的水印好好的，但是生成了pdf之后 水印的间距会有变差。这个时候，可以把你的网页窗口调整大小，使得你的网页趋紧生成的pdf，再调整水印，这样最后生成的pdf才是准确的，包括前面的提到的封面也可以这么调试（如果有偏差）。

4、如果有图表，看到别人说加上`animation: false;` 禁止动画就可以显示出来了，不然生成的pdf里的图表会是空白。

或者是（我用的方法）：

1、先用 `<div class="js-kline" style="width:700px;height:450px;" v-show="isShow"></div>` 结合echarts生成一个图表。

2、然后调用echarts的getDataURL方法生成一个图片地址放到`<img src="" id="js-img">`

```html
let echartKLine = echarts.init($('.js-kline'));

    echartKLine.setOption(option);

    window.onresize = echartKLine.resize;

    $("#js-img").attr("src",echartKLine.getDataURL())
```

最后隐藏 js-kline，显示 js-img。

相当于把图表变成了和这个图表长得一摸一样的图片。
