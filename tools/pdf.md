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
