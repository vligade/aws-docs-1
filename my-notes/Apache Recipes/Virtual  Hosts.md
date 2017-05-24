Virtual Hosts:
---------------

As a person can be known by many names, so can a Web browser support multiple Web sites.

In the Apache Configuration file, each alternate identity, and probably the "main" one as well, is known as a "Virtual Host". (sometimes written as vhost) identified with a <Virtual Host> container directive.

Depending on the name used to access the Web server, Apache responds appropriately, just as someone might answer differently
depending on whether she is addressed as "Miss Jones" or "Hey Debbie!".

If you want to have a single system support multiple web sites, you must configure Apache appropriately --- and you'll need 
to know a little bit about your system (such as the IP addresses assigned to it) in order to do it correctly.

There are two different types of virtual host supported by Apache.

    1) Address-based or IP-based
    2) Name based

1) Address-based
-----------------

    Address-based virtual host, is tied to the numeric network address used to reach the system, rather like telephone numbers.

2) Name based
--------------

    The other type of virtual host is called name-based because the server's response depends on the name by which it is 
    called.

    Ex: Consider an apartment shared by multiple room mates; you call the same number whether you want to speak to Dave, Joyce
    or Georg. Just as multiple people may share a single telephone number, multiple Web sites can share the same IP address.

    However, all IP addresses shared by multiple Apache virtual hosts need to be declared with a "NameVirtualHost" directive.


In most simple of Apache configurations, there are no Virtual Hosts. Instead, all of the directives in the configuration
file apply universally to the operation of the server.

The environment defined by the directives outside any <VirtualHost> containers is sometimes called the "default server", "main server",
or perhaps the "global server".

There is no official name for it, but it can become a factor when adding virtual hosts to your configuration.

