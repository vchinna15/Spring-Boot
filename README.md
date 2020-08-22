# Spring-Boot
Framework to create web application faster with less configuration and Embedded Web Server.
Follows Opinionated View, meaning Convention over Configuration.

Key features:
1. Embedded Servlet Container (default is Tomcat server)
2. Externalized configuration
3. healthc checks
4. Metrics
5. security

Spring Boot Build System. We need build system that has stromg dependency management. Maven or Gradle is best suited for Spring Boot. 

Spring Boot starters: they are group of dependency jar files for a particular purpose. Ex: spring-boot-starter-data-jpa.
Spring-boot-starter-web
spring-boot-starter-actuator(productionn ready features such as jealth check, metrics)

Spring Boot Configuration class: one class per application with @Configuration annotation. Or if you want auto-configuration enabled, use @SpringBootApplication or @EnableAutoonfiguration, not both.

to exclude from auto configuration: @SpringBootApplication(exclude={DataSourceAutoConfiguration.class})

TO define Spring Beans and their injected componenent:
1. Use @COmponentScan which will find all your APPLICATION COMPONENTS(@Component,@COntroller,@Service,@ Repository, etc) and automatically register as Spring Beans
2. Use @Autowired to inject DEPENDENCIES to the Spring Bean

@SpringBootApplication = @EnableAutoCOnfiguration + @ComponentScan + @Configuration

(Usually @COnfiguration is used to register(@Bean) extra beans in the context or import(@import) additional configuration classes)

DevTools(Add spring-boot-devtools module in the POM dependency):
1. Property Defaults
2. automatic restarts
3. Live relaod
4. Global settings
5. Remote applications

Executable jars can be used for production deployment. As they are self-contained, they are also ideally suited for cloud-based deployment.

Spring Boot Features:
1. SpringApplication.class (to bootstrap the application)
2. Externalized Configguration
3. Profiles
4. Logging
5. Internalization
6. Support to JSON librarires(Jackson is default)
7. Support for Web Application Development(Spring MVC)
8. Security support(MVC security(httpBasic or formLogin), OAuth2, Actuator Security)
9. SQL DB support(JdbcTemplate, spring-boot-starter-data-jpa(Hibernate, spring data jpa, spring orm), 
10. Caching (@EnableCaching, @CACHEABLE)
11. Messaging (JmsTemplate,  RabbitMQ,Apache Kafka)
12. Rest Template (for calling REST Service)
13. sending email
14. Distribuited Teansactiopn with JTA(using Atomikos Transaction Manager, Bitronix Transaction manager)
15. Testing(Utilities and annotations for testing)
16. spring-boot-starter-webservices for SOAP webserices.







