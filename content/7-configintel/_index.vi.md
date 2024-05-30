---
title : "Intellij"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

Trong bước này, sẽ thảo luận làm thế nào để cài đặt file application.properties của ứng dụng Java. Nó kết nối tới database, Amazon Cognito Service, Amazon Simpke Notification Service, để sử dụng để tạo ứng dụng.

1. Trong remote computer, mở **Intellij IDEA** 
![ConfigIntel](/images/6ConfigIntel/6.png)
2. Mở file dự án đá được tạo trước đó. 
![ConfigIntel](/images/6ConfigIntel/2.png)
3. Tìm thư mục với đường dẫn :**Airline-Booking-CodeWhisperer-PromptProject** và mở nó.
![ConfigIntel](/images/6ConfigIntel/3.png)
4. Kiến trúc của project đã được tạo để giúp bạn dễ dàng cho việc coding
![ConfigIntel](/images/6ConfigIntel/4.png)
5. Giờ ta sẽ di chuyển sang Cloudformation để lấy vài giá trị của Cognito và SNS để cung cấp cho bên trong file application.properties trong project của ta để sử dụng được vài dihcj vụ của AWS. Đi tới **Cloudformation**, click **Stacks** và chọn Cloudformation từ kết quả tìm kiếm. Trong **Outputs**, chú ý 2 giá trị **CognitoProviderName** và **SNSTopic**, Chúng tương ứng là **cognito.userpool.id** và **sns.arn**. trong aplications.properties
![ConfigIntel](/images/6ConfigIntel/5.png)
6. Đây là file application.properties , bạn cần thay thế một vài giá trị
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
7. Lấy những thông tin và thay thế bởi
   - 1, 2, 3: thông tin mà bạn kết nối tới **MySQL Workbench**, có thể lấy nó từ **Secretes manager**
   - 4: region mà chúng ta chọn cho workshop
   - 5: RDS key : xác thực của database
   - 6, 7: Lấy nó từ bước trước
![ConfigIntel](/images/6ConfigIntel/7.png)

