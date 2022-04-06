# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot Maven Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.1.8.RELEASE/maven-plugin/)
* [Spring Configuration Processor](https://docs.spring.io/spring-boot/docs/2.1.8.RELEASE/reference/htmlsingle/#configuration-metadata-annotation-processor)
* [Spring Boot Actuator](https://docs.spring.io/spring-boot/docs/2.1.8.RELEASE/reference/htmlsingle/#production-ready)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.1.8.RELEASE/reference/htmlsingle/#boot-features-developing-web-applications)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service with Spring Boot Actuator](https://spring.io/guides/gs/actuator-service/)
* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)

Just for FYI 
We are able to fix this issue by providing below variable in Java Opts and executing below Alter table scripts.

-Dorg.jbpm.correlationkey.length=4000

 

 ALTER TABLE correlationkeyinfo ALTER COLUMN name TYPE character varying(4000);

ALTER TABLE correlationpropertyinfo ALTER COLUMN name TYPE character varying(4000);

ALTER TABLE correlationpropertyinfo ALTER COLUMN value TYPE character varying(4000);

ALTER TABLE processinstancelog ALTER COLUMN correlationkey TYPE character varying(4000);

Hope this will help other who are facing similar issue.
