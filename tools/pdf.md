# PDF

wkhtmltopdf

* [wkhtmltopdf downloads](https://wkhtmltopdf.org/downloads.html)

命令格式： `wkhtmltopdf [GLOBAL OPTION]... [OBJECT]... <output file>`

1. 信息 `wkhtmltopdf -V`
2. 把一个html文件转换成PDF `wkhtmltopdf xxx.html xxx.pdf`
3. 把一个 url 指向的网页转换成PDF `wkhtmltopdf url xxx.pdf`
4. 把html文件 和 url指向的网页 转换成图片
   * `wkhtmltoimage xxx.html xxx.jpg`
   * `wkhtmltoimage url xxx.jpg`



`wkhtmltopdf --header-left "Vicky's Notes" --header-right "[date] [time]" --header-line --header-spacing 3 --footer-spacing 3 --footer-center "- 第 [page] 页-" cover cover.url toc --toc-header-text "目录" --disable-dotted-lines main.url D:\\1.pdf`

``

Kindle

```
wkhtmltopdf  --page-size A6 --margin-left 2 --margin-right 2  --enable-local-file-access  --header-left "  Vicky's Notes" --header-right "[date] [time] A6  "  --header-line --header-spacing 2 --footer-spacing 2 --footer-center "- 第 [page] 页-"    toc --toc-header-text "目录"    url   D:\\local.pdf
```
