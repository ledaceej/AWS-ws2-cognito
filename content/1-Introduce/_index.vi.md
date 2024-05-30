---
title : "Giới thiệu chung"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---


## Giới thiệu vài dịch vụ Amazon 

Trong workshop này, chúng ta sẽ dựng ứng dụng mircoservice Java springboot. Tại đây, không chỉ hướng dẫn dựng một ứng dụng mà ứng dụng còn được tích hợp nhiều dịch vụ của AWS để kiểm tra ứng dụng từ đầu đến cuối

Có một vài service bạn sẽ sử dụng trong workshop này. Đó là Cognito, SNS, Secrete Manager

- Secrete Manager giúp ta quản lý, khôi phục và thay đổi xác thực của database, API keys... xuyên suốt vòng đời của chúng
- Cognito giúp bạn triển khai xác thực người dùng, quản lý truy cập vào trong ứng dụng web và mobile. Bạn có thể nhanh chóng tạo user, truy cập tới ứng dụng trong vài phút
- Simple Notification Service gửi thông báo bằng 2 cách là A2A và A2P. A2A cung cấp 

Trong các section tiếp theo, chúng ta sẽ tìm hiểu về concept của ứng dụng kiến trúc microservice và tích hợp các dịch vụ của AWS
