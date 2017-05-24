* ----------------------------------------------------------------------------------------------------------------------------------
                                                        JAVA MAIL API
* ----------------------------------------------------------------------------------------------------------------------------------
* The JavaMail API provides a platform-independent and protocol-independent framework to build mail and messaging applications.
    The JavaMail API provides a set of abstract classes defining objects that comprise a mail system. It is optional package (standard
    extension) for reading, composing, and sending electronic messages.

* JavaMail provides elements that are used to construct an interface to a messaging system, including system components
    and interfaces. While this specification does not define any specific implementation, JavaMail does include several 
    classes that implement RFC822 & MIME Internet messaging standards. These classes are delivered as part of the 
    JavaMail class package.

* Following are some of the products supported in JavaMail API:

    * SMTP:             Acronym for Simple Mail Transfer Protocol. It provides a mechanism to deliver e-mail.

    * POP:              Acronym for Post Office Protocol. POP is the mechanism most people on the Internet use to get their mail. It                       defines support for a single mailbox for each user. RFC 1939 defines its protocol.

    * IMAP:             Acronym for Mutlipurpose Internet Mail Extensions. It is not a mail transfer protocol. Instead, it defines the                     content of what is transferred: the format of the messages, attachments, and so on. There are many different                       documents that take effect here; RFC-822, RFC-2045, RFC-2046 & RFC-2047. As a user of the JavaMail API, you                        usually don't need to worry about these formats. However, these formats do exist and are used by the programs.

    * NNTP & Others:    There are many protocols that are provided by third-party providers. Some of them are Network News Transfer
                        Protocol (NNTP), Secure Multipurpose Internet Mail Extensions. (S/MIME) etc.,
