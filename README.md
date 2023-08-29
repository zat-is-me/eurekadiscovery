# Eureka Server Initialization
    1 Create normal springBoot application
    2 Add Eureka Server depandancy to pom file
    3 Annotate the main class with @EnableEurekaServer 
    4 Configur application.properties file as following
        1 server.port=8010
        2 spring.application.name=discoveryservice
        3 eureka.instance.hostname=localhost
        4 #This make not to be discovered by other eureka discovery
        5 eureka.client.register-with-eureka=false
        6 eureka.client.service-url.defaultZone = http://${eureka.instance.hostname}:${spring.port}/eureka
    5 finally run the application and open brower call localhost:8010
