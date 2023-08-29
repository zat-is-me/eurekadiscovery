# Eureka Server Initialization
1 Create normal springBoot application
    
2 Add Eureka Server depandancy to pom file
    
3 Annotate the main class with @EnableEurekaServer 
    
4 Configur application.properties file as following
        
        server.port=8010
        spring.application.name=discoveryservice
        eureka.instance.hostname=localhost
        #This make not to be discovered by other eureka discovery
        eureka.client.register-with-eureka=false
        eureka.client.service-url.defaultZone = http://${eureka.instance.hostname}:${spring.port}/eureka
    
5 finally run the application and open brower call localhost:8010
