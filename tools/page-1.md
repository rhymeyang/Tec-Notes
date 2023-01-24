# Page 1

* [MagnetW搜索神器 磁力搜 github 开源](https://www.freedidi.com/1825.html)
* qbittorrent：https://www.qbittorrent.org github 开源
* [Surfshark VPN](https://surfshark.com/zh/)
* [ExpressVPN](https://www.expressvpn.com/)
* [Ventoy U盘启动盘制作神器](https://www.ozabc.com/it/502260.html)
* [Xtream Download Manager](https://xtremedownloadmanager.com/)



```shell

删除顽固文件代码：

DEL /F /A /Q \\?\%1
RD /S /Q \\?\%1
```

* BT种子
  * 海盗湾 www.thepiratebay.org
* 软件替代[alternative to](https://alternativeto.net/)
  * Bandicam 收费录屏软件 OBS
* 第一PPT

### WSGI

WSGI is a specification for an Application Programming Interface.

WSGI is NOT a wire protocol

WSGI is NOT an implementation of any anything

* Friends don't let friends use raw WSGI
* You still need a way to host a WSGI application
  * The development servers builtin to a framework are not good enough.
  * Installing mod\_wsgi the easy way
  * `pip install mod_wsgi`
* Run mod\_wsgi form the command line
  * `mod_wsgi-express start-server hello.wsgi`
* Run with Django management command
  * `python manage.py runmodwsgi`
  * Automatic code reloading
    * `python manage.py runmodwsgi --reload-on-changes`
  * Interactive debugger
    * `python manage.py runmodwsgi --enable-debugger`
  * Production configuration
    * `python manage.py runmodwsgi --server-root /etc/wsgi-port-80 --user www-data --group www-data --port 80 --setup-only`



