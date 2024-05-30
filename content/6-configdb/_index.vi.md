---
title : "Cấu hình DB"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

Trong hướng dẫn này, ta sẽ cấu hình MYSQL Workbench để kết nối tới máy chủ Database đã được tạo bưởi cloudformation. MySQL Workbench có thể quản lý database, truy vấn data ,..

1. Đầu tiên, ta trở lại remote computer, Mở **MySQL Workbench** 
![Config DB](/images/5ConfigDB/1.png)
2. Ta sẽ di chuyển tới màn 
![Config DB](/images/5ConfigDB/2.png)
3. Trong mục **Database** , chọn **Manage Connections** 
![Config DB](/images/5ConfigDB/3.png)
4. Nhiều thông tin mà chúng ta phải điền, ta sẽ lấy nó ở **Secretes manager**.
![Config DB](/images/5ConfigDB/4.png)
5. Chọn **Secrete manager** và chọn mục **Secretes**.
![Config DB](/images/5ConfigDB/5.png)
6. Click **RDSSecreteForApp** 
![Config DB](/images/5ConfigDB/6.png)
7. Trong **Secrete value**, sau đó đi tới **Retrieve secrete value**. Vài thông tin mà chúng ta sẽ lấy từ đây.
![Config DB](/images/5ConfigDB/7.png)
8. Trong remote computer, Click **New** và điền thông tin mà lấy từ bước trước. Các trường thông tin giống với thông tin trong **Secret value** của bước trước.

- **Connection name**, bạn có thể đặt tùy ý
- **Hostname** : **host**
- **Username** : **username**
- **Password** : **password**
![Config DB](/images/5ConfigDB/8.png)
9. Sau đó click Store in Vault, điền thông tin và click **Ok**
![Config DB](/images/5ConfigDB/9.png)
10. **Test connection** of database
![Config DB](/images/5ConfigDB/10.png)
11. Tạo kết nối thành công tới máy chủ database
![Config DB](/images/5ConfigDB/11.png)
12. Bước tiếp, ta sẽ tạo bảng và dữ liệu cho microservice. Trong mục **Database**  chọn **Connect to Database** 
![Config DB](/images/5ConfigDB/12.png)
13. Click **OK**
![Config DB](/images/5ConfigDB/13.png)
14. Bạn sẽ được chuyển tới màn khác. Bước tiếp theo ta sẽ thiết kế database và tạo data để phục vụ cho ứng dụng
![Config DB](/images/5ConfigDB/14.png)

#### Content

1. [Design DB for API find flight](6.1-DBfindflight/)
2. [Design DB for API reserve](6.2-DBreserve/)


