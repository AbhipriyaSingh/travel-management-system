The objective of the Travel and Tourism Management System project is to develop a system that automates the processes and activities of a travel and tourism agency. The purpose is to design a system using which one can perform all operations related to traveling and sight-seeing. The system allows one to easily access the relevant information and make necessary travel arrangements. Users can decide about places they want to visit and make bookings online for travel and accommodation.

![Travel and Tourism management System1](https://user-images.githubusercontent.com/81694983/120067410-17fe4080-c099-11eb-8f50-271472c619b2.png)
![Travel and Tourism management System2](https://user-images.githubusercontent.com/81694983/120067446-40863a80-c099-11eb-9b52-8d7444bc0cc4.png)
![Travel and Tourism management System3](https://user-images.githubusercontent.com/81694983/120067474-6e6b7f00-c099-11eb-9f19-699fce65663a.png)
# travel-and-tourism-management-system

## Installation instructions (Local)
 - Install Docker
 - Run Mysql docker image
 `docker run -p 3306:3306 --name mysql-local -e MYSQL_ROOT_PASSWORD=admin123 -d mysql:8.0.20`
 - Connect to mysql
 `mysql -h localhost -P 3306 --protocol=tcp -u root -p`
 - Run database migration
 ```
 create database tms;use tms;
 create table account (id int NOT NULL AUTO_INCREMENT,username varchar(255) NOT NULL,name varchar(255) NOT NULL,
 password varchar(255),security varchar(255) NOT NULL,answer varchar(255) NOT NULL,PRIMARY KEY (id));
 create table customer(username varchar(255) NOT NULL,id varchar(255),number varchar(255),name varchar(255),
 gender varchar(255),country varchar(255),address varchar(255),phone varchar(255),
 email varchar(255),PRIMARY KEY(username));
 ```
 - Build project
 `mvn clean package`
 - Run
 `java -jar ./target/travel-management-1.0-SNAPSHOT-jar-with-dependencies.jar`
