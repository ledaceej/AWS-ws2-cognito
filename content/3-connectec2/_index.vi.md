---
title : "Kết nối tới EC2"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

## Preparation steps

Tiếp theo chúng ta sẽ cài đặt EC2 để kết nối bằng RDP từ máy tính của chúng ta

1. Từ console, chọn dịch vụ **EC2**.

![ConnectEC2](/images/2connectEC@/1.png)

2. Click vào **instances running**.

![ConnectEC2](/images/2connectEC@/2.png)

3. Chọn instance hiện trên màn hình

![ConnectEC2](/images/2connectEC@/3.png)


4. Click vào **security**, và sau đó click vào **Security group** để cài đặt RDP.

![ConnectEC2](/images/2connectEC@/5.png)

5. Chọn **inbound rules** sau đó **Edit bound rules**.

![ConnectEC2](/images/2connectEC@/6.png)

6. Thêm rule

![ConnectEC2](/images/2connectEC@/7.png)

7. Trong **Type** chọn RDP và **Source** chọn **My IP** và **Save rules**.
 
![ConnectEC2](/images/2connectEC@/8.png)

8. Trở lại nơi giống như tiêu đề, và click **Connect**
![ConnectEC2](/images/2connectEC@/9.png)
9. Click vào **RDP client** và tài **remote desktop file**.


![ConnectEC2](/images/2connectEC@/11.png)
10. Mở file vừa mới download .

![ConnectEC2](/images/2connectEC@/12.png)

11. Chọn **Connect** và **Next** trong màn hình hiển thị để kết nối tới EC2, cho đến khi bạn nhập mật khẩu. Khi đó bạn cần vào dịch vụ Secret manager nơi lưu các bảo mật thông tin quan trọng như mật khẩu, API key, DB credentials và bạn sẽ tới đó để lấy mật khẩu của user ADmin để kết nối tới EC2
![ConnectEC2](/images/2connectEC@/13.png)
12. Từ **home console** chọn **AWS Secretes Manager** sau đó chọn **Secretes** Nó sẽ tới được màn hình giống như hình ảnh bên dưới. Chọn **EC2instancesSecret** .

![ConnectEC2](/images/2connectEC@/14.png)
13. Tìm mục **Secret value** và chọn **Retrieve secret value**.
![ConnectEC2](/images/2connectEC@/15.png)
14.  Sao chép **pass_word**, đó là mật khẩu của tài khoản admin để kết nối tới EC2

![ConnectEC2](/images/2connectEC@/16.png)
15.  Đăng nhập tới Ec2 bằng cách dùng **Administrator** như username. Nhập mật khẩu mà ta đã lấy được từ bước trước

![ConnectEC2](/images/2connectEC@/17.png)
16. Bạn đã đăng nhập thành công, bạn sẽ sử dụng nó trong các bước tiếp theo.
![ConnectEC2](/images/2connectEC@/20.png)






