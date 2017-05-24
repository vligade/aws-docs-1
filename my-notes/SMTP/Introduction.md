* ------------------------------------------------------------------------------------------------------------------------------
* SMTP is an acronym for Simple Mail Transfer Protocol. It is an Internet standard for electronic e-mail transmission across 
    Internet Protocol (IP) networks.

* SMTP uses TCP port 25.

* SMTP connections secured by SSL are known by the shorthand as SMTPS, though SMTPS is not a protocol in its own right.

* JavaMail API has package "com.sun.mail.smtp" which act as SMTP protocol provider to access an SMTP Server.
* ------------------------------------------------------------------------------------------------------------------------------

* ------------
* SMTPMessage
* ------------

    This class is a specialization of the MimeMessage class that allows you to specify various SMTP options and 
    parameters that will be used, when this message is sent over SMTP.

* -----------------
* SMTPSSLTransport
* -----------------

    This class implements the Transport abstract clsss using SMTP over SSL for message submission and transport.

* --------------
* SMTPTransport
* --------------

    This class implements the Transport abstract class using SMTP for message submission and transport.

* --------------
* Exceptions:
* --------------

    SMTPAddressFailedException      ---  This exception is thrown when the message cannot be sent.

    SMTPAddressSucceededException   ---  This exception is chained off a SendFailedException when the mail.smtp.reportsuccess property                                      is true.

    SMTPSenderFailedException       ---  This exception is thrown when the message cannot be sent.

    SMTPSendFailedException         ---  This exception is thrown when the message cannot be sent. The exception includes the sender's                                      address, which the mail server rejected.


* The ==> com.sun.mail.smtp ==> provider use SMTP Authentication optionally. To use SMTP authentication you'll need to set the   
    ==> mail.smtp.auth ==> properly or provide the SMTP Transport with a username or password when connecting to the SMTP Server.

* You can do this using one of the following approaches;

    * Provide an Authenticator object when creating your mail Session and provide the username and password information during the
      Authenticator callback. 

      * mail.smtp.user ==> property can be set to provide a default username for the callback, but the password will still need
        to be supplied explicitly. This approach allows you to use the static Transport send method to send messages. For example;

        * Transport.send(message);


    * Call the "Transport" connect method explicitly with username and password arguments. For example;

        Transport tr = session.getTransport("smtp");
        tr.connect(smtphost, username, password);
        msg.saveChanges();
        tr.sendMessage(msg, msg.getAllRecipients());
        tr.close()

    The SMTP protocol provider supports the following properties, which may be set in the JavaMail Session object. The properties 
    are always set as strings. for example;

        props.put("mail.smtp.port", "587");

* ------------------------------------------------------------------------------------------------------------------------------
*       NAME                            TYPE                DESCRIPTION
* ------------------------------------------------------------------------------------------------------------------------------

    mail.smtp.user                      String              Default user name for SMTP.

    mail.smtp.host                      String              The SMTP server to connect to.

    mail.smtp.port                      int                 The SMTP server port to connect to, if the connect() method doesn't
                                                            explicitly specify one. Default to 25.

    mail.smtp.connectiontimeout         int                 Socket connection timeout value in milliseconds. Default is infinite
                                                            timeout.

    mail.smtp.timeout                   int                 Socket I/O timeout value in milliseconds. Default is infinite timeout.

    mail.smtp.from                      String              Email address to use for SMTP MAIL command. This sets the envelope 
                                                            return address. Defaults to msg.getForm() or 
                                                            InternetAddress.getLocalAddress().

    mail.smtp.localhost                 String              Local host name used in the SMTP HELO or EHLO command. Defaults to 
                                                            InetAddress.getLocalHost().getHostName(). Should not normally need to
                                                            be set if your JDK and your name service are configured properly.

    mail.smtp.localaddress              String              Local address (host name) to bind to when creating the SMTP socket.
                                                            Defaults to the address picked by the Socket class. Should not normally
                                                            need to be set.

    mail.smtp.localport                 int                 Local port number to bind to when creating the SMTP socket. Defaults
                                                            to the port number picked by the Socket class.

    mail.smtp.ehlo                      boolean             If false, do not attempt to sign on with the EHLO command. Defaults to 
                                                            true.

    mail.smtp.auth                      boolean             If true, attempt to authenticate the user using the AUTH command. Defaults
                                                            to true.

    mail.smtp.auth.mechanisms           String              

* ------------------------------------------------------------------------------------------------------------------------------                                               
