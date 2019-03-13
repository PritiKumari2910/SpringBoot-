# This SpringBootApp is made using Spring Initializer and Spring Tool Suite-

Dependencies Used from Spring Initializer(https://start.spring.io/):
1> H2
2> REST Repositories
3> Rest Repositories with HAL Browser
4> JPA

H2 database is used and its mapping is done in application.properties using :
spring.datasource.url=jdbc:h2:mem:wines
This will create the DB wines and data.sql will add the dummy details to this DB, which we will be manipulating in this app and the output is in JSON format which can be seen in browser directly.

Output on Browser can be seen due to Rest Repository HAL Browser which provides an easy way to check and perform operations on resources:

Working:
Input(From H2 database) -> Wine entity is defined in Wine.java  -> CRUD operations are performed by CrudRepository interface which is  defined in RestRepository interface.-> Output can be checked on browser as its a REST API 

To get details:
http://localhost:8080/wines/
http://localhost:8080/browser/index.html#/  <- to check all the resources, try get , non-get <POST,DELETE>
http://localhost:8080/browser/index.html#http://localhost:8080/wines/
