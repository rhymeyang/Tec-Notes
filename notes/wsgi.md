# WSGI

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
