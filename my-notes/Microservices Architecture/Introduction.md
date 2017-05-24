What is Microservice ?
----------------------

Microservice architectural style is an approach to developing a single application as a suite of small services, 
each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API.

What is Microservice ?
----------------------

The Microservice is built around business capabilities and is independently deployable by fully automated deployment
machinery.

There is a bare minimum of centralized management of these services, which may be written in different programming languages
and use different data storage technologies. For example, In an ecommerce site, Payment service could be written in C++,
while Order management service could be written in Java.

Amazon is regarded as the first company to get microservices and APIs right.

Microservice - Simple Understanding:
------------------------------------
Application functionality, whenever possible, should be broken into lightweight, discrete services, each of which 
meets a particular business-focused concern.

An application is decomposed into micro services based on 2 categories;

* Decompse by business capability:
* ----------------------------------
* The services are created based on the business capabilities. For example in Retailer 
* Ecommerce - billing, payment, order management and promotions are different business capabilities, which could be 
* made into separate services.

* Decompose by subdomain:
* --------------------------
* Domain driven design advocates modelling based on the reality of the business and relevant to use cases.
* 

Wrong decomposition could impact at architectural level.



