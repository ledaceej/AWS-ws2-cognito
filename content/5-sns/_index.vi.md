---
title : "Simple Notification Service"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

Ở bước này, chúng ta sẽ thảo luận làm thế nào để tạo đăng kí, ta sẽ sử dụng nó để xác nhận việc gọi API thành công

1. Từ console, chọn **Simple Notification Service**
![SNS](/images/4SNS/1.png)
2. Chọn mục **Topics** 
![SNS](/images/4SNS/2.png)
3. Bạn có 1 topic đã tạo từ Cloudformation, sau đó click tới topic
![SNS](/images/4SNS/3.png)
4. Trong topic **reservation-success** , click **Create subcription** 
![SNS](/images/4SNS/4.png)
5. Chọn protocol **Email**, **Endpoint** là email mà mình muốn nhận thông báo. Sau đó click **Create subscription**.
![SNS](/images/4SNS/5.png)
6. Kiểm tra email rồi click **Confirm subscription** 
![SNS](/images/4SNS/6.png)
7. Bạn sẽ tới trang, sẽ thông báo cho bạn rằng subscription đã được xác nhận, bạn có thể unsubcribe
![SNS](/images/4SNS/7.png)
8. Bạn đã cài đặt thành công SNS topic, nó sẽ nhận email để thông báo API của bạn đã được gọi thành công
![SNS](/images/4SNS/8.png)


