---
title : "Kiểm thử API"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 8.1.2 </b> "
---

1. Sau khi viểt API, hãy kiểm thử nó. Đầu tiên tìm file **FlightBookingApplication.java** bằng đường dẫn **src/main/java/com/airlines/catalog/** để mở nó
![Testapi Find flight](/images/7TestFindFlightAPI/1.png)
2. Click vào nút
![Testapi Find flight](/images/7TestFindFlightAPI/2.png)
3. Chọn **Run 'FlightBookingMain'**
![Testapi Find flight](/images/7TestFindFlightAPI/3.png)
4. Chờ vài giây để hoàn thành khởi động ứng dụng
![Testapi Find flight](/images/7TestFindFlightAPI/4.png)
5. Mở **PostMan**  để kiểm thử API
![Testapi Find flight](/images/7TestFindFlightAPI/5.png)
6. Đầu vào là URL, dán CURL dưới đây đã được chuẩn bị từ trước để tiết kiệm thời gian của bạn. Nó gồm đầu vào của thâm số cho việc gọi API
![Testapi Find flight](/images/7TestFindFlightAPI/7.png)
Đây là **CURL**
```
curl --location 'localhost:8090/flight?departureDate=2023-08-01&departureAirportCode=LHR&arrivalAirportCode=CDG' \
--header 'Authorization: eyJraWQiOiJLQzh0Zzd0VHcraDJoVXAzeHFUNmJybHV6SUloT2JNZWtoZmc5MVNPd2swPSIsImFsZyI6IlJTMjU2In0.eyJhdF9oYXNoIjoiWUpzYVFjaDNlbGt1R2Y3bW9BT0RtUSIsInN1YiI6ImM1OTVhNDEzLTk5NmQtNGFkNi1hNTFiLTVhNTk3ZjE4MTM0YSIsImVtYWlsX3ZlcmlmaWVkIjp0cnVlLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0xLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMV9QTU9zUlBLM1kiLCJjb2duaXRvOnVzZXJuYW1lIjoibGVkYWNkZXB0cmFpIiwiYXVkIjoiNGk3aWJvYzI0aWpxYnNxNTI5ZmI3cG5kOGwiLCJldmVudF9pZCI6IjI4OTVlNWJjLTE4MWYtNDIyOS1hNGFjLTA3MWE3MWJmYjQxNiIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNzExNzM5MzA3LCJuYW1lIjoibGUgZHVjIGFuaCIsImV4cCI6MTcxMTc0MjkwNywiaWF0IjoxNzExNzM5MzA3LCJqdGkiOiJkOTgzMzMyNC1mOGJlLTRiZGYtODM5MC1mMThkYmMwZTI3MmEiLCJlbWFpbCI6ImxlZGFjZGVwdHJhaUBnbWFpbC5jb20ifQ.E478H8NzHp1a2nt5MmrF8Qe52grqJ8wUk-55INdlaiT2arQQe8Aj1JeIbt8QSs14KTF5iD4EEoLMkkoqDi4JvCG7IU8BYCb-ygEEd6IazVanqO7acduh8xfWSosY3RCrt3xZSdDUHHXLicCBo8yz0Z1TqAWPfxgN1CV46ErRh_zF05HJ1c77ybqUyR5FVyJEGQDs9XkX0MR9ol6rJTWylK2e448MbsHtQ17xfDvOmS_RSUrN4r7zHVmxK2p_23EQ9C54gTs-GXz478JT9T_uR1JXONmtaLZEi7-lfrpB2mkmLd9MQ5dgJfKFd59fd4bV0IKB3G6t2d0ZMnowjitttw'
```
7. Màn hình sẽ như sau
![Testapi Find flight](/images/7TestFindFlightAPI/8.png)
8. Click vào **Headers**, quan sát key **Authorization** là token giống như một phần của  **curl** mà tôi đã nhắc tới trước đó. Nó là JWT token đã hết hạn, Giờ bạn phải lấy JWT token mới.
![Testapi Find flight](/images/7TestFindFlightAPI/9.png)
9. Trở lại **Amazon Cognito** chọn mục **User pools** và click **TwoAuthen-UserPool**  
![Testapi Find flight](/images/7TestFindFlightAPI/10.png)
10. Click **App integration** 
![Testapi Find flight](/images/7TestFindFlightAPI/12.png)
11. Cuộn xuống dưới **App client and analysts** chọn **App client**
![Testapi Find flight](/images/7TestFindFlightAPI/13.png)
12. Trong mục **Hosted UI**, click  **View Hosted UI**
![Testapi Find flight](/images/7TestFindFlightAPI/14.png)
13. Bạn sẽ sang trong tab đăng nhập mới, Điền thông tin tài khoản đã tạo từ trước đó rồi click **Sign in**
![Testapi Find flight](/images/7TestFindFlightAPI/15.png)
14. Sao chép URL vào Notedpad 
![Testapi Find flight](/images/7TestFindFlightAPI/16.png)
15. Cắt **id_token**
![Testapi Find flight](/images/7TestFindFlightAPI/17.png)
16. Sao chép **id_token**. Token có hiệu lực trong 1 tiếng, Nếu nó hết hạn, thì bạn có thể lấy lại nó bằng các quay lại thực thi lại như các bước bên trên
![Testapi Find flight](/images/7TestFindFlightAPI/18.png)
17. Dán nó vào giá trị của **Authorization**
![Testapi Find flight](/images/7TestFindFlightAPI/19.png)
17. Giờ bạn đã có đầy đủ thông tin cần cho API click **Send** quan sát kết quả đầu ra 
![Testapi Find flight](/images/7TestFindFlightAPI/20.png)
18. Đây là thông tin của chuyến bay. Bạn đã gọi thanh công API tìm chyến bay.
![Testapi Find flight](/images/7TestFindFlightAPI/21.png)

