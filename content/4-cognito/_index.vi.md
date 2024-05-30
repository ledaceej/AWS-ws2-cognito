---
title : "Cài đặt Cognito"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

## Cài đặt Cognito

In this step, we will set Cognito for creating user,password. Using it to authenticate to connect application that like enterprise application.


1. Từ màn hình chính, chọn **Cognito** 
![Cognito](/images/3Cognito/1.png)
2. Click vào **User pool** và chọn user pool có tên là **TwoAuthen-UserPool**.
![Cognito](/images/3Cognito/2.png)
3. Chọn **App integration**
![Cognito](/images/3Cognito/3.png)
4. Cuộn xuống bên dưới và chọn **UserPoolClient**
![Cognito](/images/3Cognito/4.png)
5. Bên trong mục **Hosted UI**, chọn vào **View Hosted UI**
![Cognito](/images/3Cognito/5.png)
6. Bạn sẽ di chuyển tới tab mới . Đây là lần đầu chúng ta tới đây vì vậy đầu tiên chúng ta phải **Sign up**.
![Cognito](/images/3Cognito/6.png)
7. Điền thông tin để tạo user
![Cognito](/images/3Cognito/7.png)
8. Một email được gửi tới, hoàn thành để tạo tài khoản thành công
![Cognito](/images/3Cognito/8.png)
9. Điền code bạn nhận được và click **Confirm account**.
![Cognito](/images/3Cognito/9.png)
10. Giờ chúng ta sẽ chuyển hướng tới **localhost:8080** . Bỏ qua lỗi bởi trang web, Ta sẽ trở lại đây và một lúc nữa để lấy được token từ link URL cho mục đích kiểm thử API
![Cognito](/images/3Cognito/10.png)


