# Eureka Server Initialization
1 Create normal springBoot application using start.spring.io
    https://start.spring.io/

2 Add Eureka Server dependency to pom file
`   
    <dependency>
        <groupId>org.springframework.cloud</groupId>
        <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
    </dependency>`
    
3 Annotate the main class with @EnableEurekaServer 
    
4 Configur application.properties file as following
        
        server.port=8010
        spring.application.name=discoveryservice
        eureka.instance.hostname=localhost
        #This make not to be discovered by other eureka discovery
        eureka.client.register-with-eureka=false
        eureka.client.service-url.defaultZone = http://${eureka.instance.hostname}:${spring.port}/eureka
    
5 finally run the application and open browser call 
    http://localhost:8010
