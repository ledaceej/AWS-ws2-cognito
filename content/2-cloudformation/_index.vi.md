---
title : "CloudFormation"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

## Cloudformation
1. Tải format Cloudformation **cfn-basic-setup.yaml** từ địa chỉ sau. Cloudformation này sẽ cài đặt tất cả kiến trúc mà chúng ta cần cho workshop này
[DownLoad here](https://ws-assets-prod-iad-r-iad-ed304a55c2ca1aee.s3.us-east-1.amazonaws.com/fa91011f-2da1-4cd9-a3ba-57891dcaa6f5/cfn-basic-setup.yaml )

2. Focus how infras of file .yaml

3. Ở console, tìm kiếm Cloudformation và chọn dịch vụ Cloudformation


![Cloudformation](/images/1cloudformation/1x.png)
4. Các region khác sẽ không khả khi khi ta tạo các tài nguyên của ta trong cloudformation, vì vậy đầu tiên chúng ta thay đổi region sang **us-east-1**

![Cloudformation](/images/1cloudformation/1.png)
5. Sau đó click **Create stack**. 

![Cloudformation](/images/1cloudformation/2.png)
6. Click chọn file  **cfn-basic-setup.yaml** mà chúng ta đã tải. rồi click **Next**

![Cloudformation](/images/1cloudformation/3.png)

7. Điền đầy đủ thông tin name, và các cài đặt khác sẽ để mặc định **Next**
![Cloudformation](/images/1cloudformation/4.png)

8. Tích chọn Acknowledge all the options và click **Submit**
![Cloudformation](/images/1cloudformation/5.png)

9. Bạn sẽ chuyển sang màn khác, và chờ một thời gian khoảng 10 phút để hoàn thành quá trình tạo
![Cloudformation](/images/1cloudformation/6.png)

10. Màn hình sau khi đã khởi tạo thành công
![Cloudformation](/images/1cloudformation/7.png)
