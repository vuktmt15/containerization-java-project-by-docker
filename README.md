# Containerizing Java application with Apache tomcat, Nginx and Mysql server

## Steps   

- 1. Fetch source code from git repository
- 2. Create Dockerfiles for nginx, tomcat and mysql server and build images
- 3. Create the docker-compose file to build and test the services
- 4. Push the docker images onto dockerhub if everything is ok

## Prerequisites

- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

## Technologies 

* Web Application
  * Spring MVC
  * Spring Security
  * Spring Data JPA
  * JSP  
* Maven
* MySQL 
* RabbitMQ 
* Memcache


``` 
        ┌─────┐   
        │NGINX│             
        └─────┘
          |↑
          ||   _______┌─────┐
          ||  //-----→│MySQL│←-----
          ↓|  ↓|      └─────┘----||
    ┌─────────────┐     |↑       ||
    │Tomcat_Server│     ||       ||
    └─────────────┘     ↓|       ||
          |↑        ┌────────┐   ||
          ||        │Memcache│   ||
          ||        └────────┘   || 
          ↓|         ↑|          ||
      ┌────────┐     //          ||
      │RabbitMQ│____//           ||
      └────────┘←----            //
          |↑                    //
          ||___________________//
          ----------------------     
```  

## Command 

```
docker-compose up -d
```


# containerization-java-project-by-docker
