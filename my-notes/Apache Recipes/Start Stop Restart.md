Problem:
---------

You want to be able to start and stop the server at need, using the appropriate tools.

Solution:
----------

On Unixish systems, use the "apachectl" script.
On Windonws, use the options in the Apache folder of the Start Menu.

Discussion:
------------
The basic Apache package includes tools to make it easy to control the server. For Unixish Systems, this is usually a script
called apachectl, but prepackaged distributions may replace or rename it.

It can perform one action at a time, and the action is specified by the argument in the command line. 

The options of interest are;

1) apachectl start
---------------------
    This will start the server if it isn't already running. If its running, this option has no effect and may produce a warning
    message.

2) apahcectl graceful
----------------------
    This option causes the server to reload its configuration files and gracefully restart its operation. Any current connections in 
    progress are allowed to complete. The server will be started, if it isn't running.

3) apachectl restart
---------------------
    Like the graceful option, this one makes the server reload its configuration files. However, existing connections are 
    terminated immediately. If the server isn't running, the command will try to start it.

4) apachect1 stop
------------------
    This shuts the server down immediately. Any existing connections are terminated at once.
