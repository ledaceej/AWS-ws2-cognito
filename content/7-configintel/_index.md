---
title : "Intellij"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

In this guide, we will discuss how to setting file application.properties of Java application project. It is to connect to database, Amazon Cognito Service, Amazon Simple Notification Service, Amazon Relational Database Service to use for creating microservices

1. In the remote computer, open **Intellij IDEA** 
![ConfigIntel](/images/6ConfigIntel/6.png)
2. Open file project that created before. 
![ConfigIntel](/images/6ConfigIntel/2.png)
3. Find folder with path: .It is named **Airline-Booking-CodeWhisperer-PromptProject** then open it.
![ConfigIntel](/images/6ConfigIntel/3.png)
4. Structure of project was created to help you easy for coding
![ConfigIntel](/images/6ConfigIntel/4.png)
5. Now, we move on Cloudformation to take some value of Cognito and SNS to provide for application,properties in my project to use these services. Go to **Cloudformation**, click **Stacks** and chose Cloudformation from the search results. In **Outputs**, attend 2 value **CognitoProviderName** and **SNSTopic**, That are respectively **cognito.userpool.id** and **sns.arn**. in aplications.properties
![ConfigIntel](/images/6ConfigIntel/5.png)
6. This is my application.properties file, you need replace some value to your value
 ```
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=none
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect

spring.datasource.url=cw-sample.c7aqu420y9mw.us-east-1.rds.amazonaws.com
spring.datasource.username=admin
spring.datasource.password=MqzSH]1ce%
spring.datasource.driver-class-name=com.mysql.jdbc.Driver


server.port = 8090

aws.region=us-east-1
secretmanager.key=RDSSecretForApp
cognito.userpool.id=cognito-idp.us-east-1.amazonaws.com/us-east-1_PMOsRPK3Y
sns.arn=arn:aws:sns:us-east-1:992382617520:reservation-success
 ```
7. Take some information and replace with that
   - 1, 2, 3: information that you connect to **MySQL Workbench**, you can retake it from **Secretes manager**
   - 4: your region you chose to do this workshop
   - 5: RDS key : credential of database
   - 6, 7: We take it from the previous step
![ConfigIntel](/images/6ConfigIntel/7.png)

