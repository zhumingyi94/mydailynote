# Java Spring

### Overview
>[!question]- What is Java Actuator 
>It just the tools that helps us understand about the system and provide several endpoints, you can check it in [List of enpoints](www.luv2code.com/actuator-endpoints)

>[!question]- How to expose all endpoints
>![[Pasted image 20240731173142.png | center]]

>[!question]- How to customize Spring Security 
> ```java 
> spring.security.user.name=nhatdo94
> spring.security.user.password=something
>```
>```maven
>management.endpoints.web.exposure.exclude=health, info
>```

 >[!question]- How to inject custom application properties
 >```java
 >@RestController
 >public class FunRestController {
 >@Value("${coach.name}")
 >}private String coachName;
 >@Value("${team.name}")
 >private String teamName;
>```

>[!question]- How to decide which log level to use ?
>![[Pasted image 20240801051356.png | center]]


>[!question]- What you can change in Core Properties
>Log level and log file path, log file name

>[!question]- What you can change in Web Properties
>```java
>// Change port
>server.port=7070
>// Context path of the application
>server.servlet.context-path=/my-silly-app
>// Session imeout 
>server.servlet.session.timeout=15m
>```

>[!question]- What can you change in Actuator Properties
>```java
>management.endpoints.web.exposure.include=*
>// Endpoints to exclude by name or wildcard
>management.endpoints.web.exposure.exclude=beans, mapping
>// Base path for actuator endpoints
>management.endpoints.web.base-path=/actuator
>```

>[!question]- What can you change in Security Properties
>```java
>// Default user name 
>spring.security.user.name=admin
>spring.security.user.password=topsecret
>```

>[!question]- What can you change in Data Properties
>```java
>// JDBC URL of the database
>spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce
>// Login username of the database
>spring.datasource.username=scott
>// Login password of the database
>spring.datasource.password=tiger
>```

>



