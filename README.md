# sping-boot-microservices
is a microservice application with User authentication, National Id and Passport
service, sms service and some other service are under processing like payment service, location
service etc. 
All of the services are separate application which can be operated in a single page
Angular UI. All the services can be reused to any other application.

## Features:
- RESTful Microservices
- JWT authentication
- Cross-Origin Resource Sharing
- Spring Boot, Spring Data JPA, Spring Security
- Angular
- Java 8 (recommended), 10
- Docker

## Services:
 - NID and Passport service
 
 - [User Authentication service](https://github.com/hnjaman/sping-boot-microservices/tree/master/user-authentication)
  
 - [SMS service](https://github.com/hnjaman/sping-boot-microservices/tree/master/sms-service)
  
 - [Location service](https://github.com/hnjaman/sping-boot-microservices/tree/master/location-service) (coming soon)
 
 - Payment service (Coming)
  
##  How to run?

```
# Set mysql database 
mysql -u root -p
create user 'cfbd'@'localhost' identified by '1234';
grant all privileges on *.* to 'cfbd'@'localhost';
create database if not exists user_db;
# Initially tables and data will be created automatically by Java Persistence API
# Update and new operation can be happened from UI
```

```
# Build and run NID, Passport services  
mvn clean install
mvn spring-boot:run
# Go to http://localhost:8888/nids; http://localhost:8888/passports
```

```
# Build and run user authentication services  
mvn spring-boot:run
# Go to http://localhost:8777/
```

```
# Run sms service
cd sms-service
mvn spring-boot:run
# Go to http://localhost:8999/sms
```

```
# All service are started use them on Angular UI
# Run Angular User interface
cd microservice-ui
# install node package manager (just for first time)
npm install
ng s --open
# It will open automatically in http://localhost:4200/home
```

## Copyright & License

MIT License, see the link: [LICENSE](https://github.com/hnjaman/sping-boot-microservices/blob/master/LICENSE) file for details.
