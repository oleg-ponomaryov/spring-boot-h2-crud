# spring-boot-h2-crud

This project explains CRUD (**C**reate, **R**ead, **U**pdate, **D**elete) operations using spring boot and H2 in-memory database.
In this app we are using Spring Data JPA for built-in methods to do CRUD operations.     
`@EnableJpaRepositories` annotation is used on main class to Enable H2 DB related configuration, which will read properties from `application.properties` file.


1. Pre-requisites and how to build.
	- Install Maven. Maven is Java build tool (similar to Gradle). Easiest way to install maven: brew update & brew install maven
	- mvn clean install
   
2. Properties file (could be just left unchanged)
    Reading H2 DB related properties from **application.properties** file and configuring JPA connection factory for H2 database.  

     server.port=8088
    
     spring.datasource.url=jdbc:h2:mem:sampledb
     spring.datasource.driverClassName=org.h2.Driver
     spring.datasource.username=sa
     spring.datasource.password=password
     spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
    
     spring.h2.console.enabled=true
    
     #spring.data.rest.base-path=/phone
     spring.data.rest.base-default-page-size=10
     spring.data.rest.base-max-page-size=20
    
     springdoc.version=1.0.0
     springdoc.swagger-ui.path=/swagger-ui-custom.html 
   
3. To run: ./start.sh
4. To test (in separate session-> curl or in browser): curl http://localhost:8088/employees 
