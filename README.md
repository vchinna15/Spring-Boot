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

(Usually @COnfiguration is used to register(@Bean) extra beans in the context or import(@import) additional configuration classes0





