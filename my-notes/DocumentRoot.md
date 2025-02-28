DocumentRoot ::: Directive
---------------------------
Directory that forms the main document tree visible from the web.

Syntax: 
-------
DocumentRoot <directory-path>

Default value will be taken as: "/usr/local/apache/htdocs"

Context: service config, virtual host

Status: Core

Module: core


Explanation:
------------

This directive sets the directory from which httpd will serve files. Unless matched by a directive like "Alias", the server appends
the path from the requested URL to the document root to make the path to the document;

Ex:

DocumentRoot "/usr/web"

then an access to http://my.example.com/index/html refers to "/usr/web/index.html".

If the directory path is not absolute then it is assumed to be relative to the "ServerRoot".