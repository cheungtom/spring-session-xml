It is the end to end setup of Java program and AWS ElastiCache Redis.

For Java program, it is based on Spring Boot, Spring Framework 4, spring-session-data-redis,
spring-session, spring-data-redis etc

The program compiled by Maven and JDK 1.8 or above, and tested on Tomcat 9

For local test, just use http://localhost:8080/manager/html Tomcat app to deploy the WAR,
surely you need to setup a local Redis server at your laptop

For AWS test, I setup an EC2 instance with Amazon Linux AMI, install the Tomcat, use
http://<ec2-public-dns>/manager/admin to deploy the WAR, surely, you need to create a
ElastiCache Redis (non-cluster mode) at your VPC of your AWS account

1. Java Program reference:
https://www.concretepage.com/spring-session/spring-session-redis-servlet-integration-example

Thanks for the author of above link. The code at this GitHub is based from above link,
and just with a few change to make it can be compiled by Maven and run on Tomcat, connect
to AWS ElasiCache Redis, also adding some debugging message. 

The program IP right is surely belongs to author of the above link.

- Git clone the program


- Command line, run: 
   mvn clean install

- Import into Eclipse:
  Command line, run
  mvn eclipse:eclipse

  Import Maven project into Eclipse

2. AWS ElastiCache Redis setup reference:  
https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/Clusters.Create.CON.Redis.html
