The Architecture of Tomcat:
---------------------------

A Tomcat instance or server, is Top Level component in Tomcat's container hierarchy. Only one Tomcat instance can live in a single 
Java Virtual Machine (JVM). This approach makes all other Java applications, running on the same physical machine as Tomcat Server to be safe, in case the Tomcat and/or its JVM crashes.

Tomcat instance consists of grouping of the applications containers, which exist in the well-defined hierarchy.

The Key component in that hierarchy is the Catalina servlet engine. 

Catalina is the actual Java Servlet container implementation as specified in Java Servlet API. Tomcat 7 implements Servlet API 3.0. (at the time of writing)

<Server>
    <Service>
        <Connector/>
        <Engine>
            <Host>
                <Context></Context>
            </Host>
        </Engine>
    </Service>
</Server>


A Tomcat Instance can be broken down into a set of containers that includes;

1) Server

2) Service

3) Connector

4) Engine

5) Host

6) Context


Server:
--------

The first container element referenced in this snippet is the <Server> element. It represents the entire Catalina Servlet engine
and is used as a top-level element of a single Tomcat Instance. The <Server> element may contain one or more <Service> containers.


Service:
--------

The next container element is the "Service" element. This comprises of one or more <Connector> elements that share a single
<Engine> element. N-number of <Service> elements may be nested inside a single <Server> element.


Connector:
----------

The next type of element is the <Connector> element, which defines the class that does the actual handling of requests and responses
to and from a calling client application.

The Engine:
-----------

The Third container element is the <Engine> element. Each defined <Service> can have only one <Engine> element, and this single
<Engine> component handles all requests received by all of the defined <Connector> components defined by a parent service.


The Host:
---------
The <Host> element defines the virtual hosts that are contained in each instance of Catalina <Engine>. Each <Host> can be parent
to one or more web applications, with each being represented by a <Context> component.


The Context:
------------
The <Context> element is the most commonly used containers in a Tomcat Instance. Each <Contex> element represents a web-application,  that is running within a defined <Host>. There is no limit to the number of contexts that can be defined within a <Host>.


---------------------------
TOMCAT DIRECTORY STRUCTURE
---------------------------

The Tomcat installation directory is referred to as CATALINA_HOME. It is assumed that each of these directories is contained 
within the CATALINA_HOME directory.

/bin            ==> Contains the startup and shutdonw scripts for both Windows and Linux. Jar files with classes required for tomcat 
                    to start are also stored here.

/conf           ==> Contains the main configuration files for Tomcat. The two most important are server.xml and the global web.xml.


/lib            ==> Contains the Tomcat Java Archive (jar) files, shared across all Tomcat components. All web applications deployed to
                    Tomcat can access the libraries stored here. This includes the Servlet API and JSP API libraries.


/logs           ==> Contains the Tomcat's log files.


/temp           ==> Temporary file system storage.


/webapps        ==> The directory where all web applications are deployed, and where you place your WAR file when it is ready for 
                    deployment.

/work           ==> Tomcat's working directory where Tomcat places all servlets that are generated from the JSPs. If you want to see
                    how a particular JSP is interpreted, look in this directory.