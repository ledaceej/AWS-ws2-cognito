---
title : "Kiểm thử API"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 8.2.2 </b> "
---



1. Sau khi hoàn thành API, click return button. Thời gian chạy khoảng vài giây
![Testapi Reserve](/images/8TestReserveAPi/1.png)
2. Sao chép **curl** đã chuẩn bị dưới đây
```
curl --location 'localhost:8090/reserve' \
--header 'Authorization: eyJraWQiOiJLQzh0Zzd0VHcraDJoVXAzeHFUNmJybHV6SUloT2JNZWtoZmc5MVNPd2swPSIsImFsZyI6IlJTMjU2In0.eyJhdF9oYXNoIjoiYXUzNFdHZm5GeUs0YVdpa1gxa2lkdyIsInN1YiI6ImM1OTVhNDEzLTk5NmQtNGFkNi1hNTFiLTVhNTk3ZjE4MTM0YSIsImVtYWlsX3ZlcmlmaWVkIjp0cnVlLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0xLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMV9QTU9zUlBLM1kiLCJjb2duaXRvOnVzZXJuYW1lIjoibGVkYWNkZXB0cmFpIiwiYXVkIjoiNGk3aWJvYzI0aWpxYnNxNTI5ZmI3cG5kOGwiLCJldmVudF9pZCI6IjE4YmUyMmM2LTdkZjUtNDg1Ny04YmE5LTkyZjQwNzhkZWZmZSIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNzExNzQ0NDAwLCJuYW1lIjoibGUgZHVjIGFuaCIsImV4cCI6MTcxMTc0ODAwMCwiaWF0IjoxNzExNzQ0NDAwLCJqdGkiOiI1NDhjZjlmZS03ZTc5LTQ4ZWUtYjJlZi1kNjVjZjM1MzU0NjEiLCJlbWFpbCI6ImxlZGFjZGVwdHJhaUBnbWFpbC5jb20ifQ.G3cTAq-4zaDGoOXm8PeScb1hsKWZrSJwRaHolbhCIynuyLwqvyDxijsvSTQgeRYbzn4ZPqMt1RJ22XjvA4n7gTrFKAmcudhM7XndGVsJadZ2ks29VvnIJQXmxu7a66R5GTCucgibbkNBAPI9vUOZl5-QuF6UopBDflCFKtQPlwTW5rtR8bhGMVnEZlTundBLwg3wZcNve4ChyIePMGtOURCW7aSsIh3VGU7whFVK3jAR-I_zm4FtQIwBI0grgEjxxizr5u-3HD4o30uT5X_dZQmguyYi9Rhiq_uAL6Be1RmmYl74KYCDZsKmZdLIIVDIM5LvGbxXt8zpvuo9JosiCA' \
--header 'Content-Type: application/json' \
--data-raw '{
    "flightId": 1,
    "travelClass": "Economy",
    "ticketPrice": 1000,
    "currencyCode": "USD",
    "paymentMode": "Credit Card",
    "contactNumber": "+123456789012",
    "contactEmail": "ledacdeptrai@gmail.com",
    "reservationStatus": "Confirmed",
    "reservationDate": "2022-01-01",
    "reservationTime": "12:00:00",
    "paymentStatus": "Paid",
    "passengerId": 1,
    "lastName": "Last Name is required",
    "firstName": "First Name is required",
    "age": "30",
    "gender":"Male"
}'
```
Từ URL, dán **curl**
![Testapi Reserve](/images/8TestReserveAPi/2.png)
3. Trong mục **Headers**, thay thế **Authorization** giống [**Testing Find Flight API**]
![Testapi Reserve](/images/8TestReserveAPi/3.png)
4. Click **send** và quan sát kết quả
![Testapi Reserve](/images/8TestReserveAPi/4.png)
5. Kiểm tra email bạn sử dụng để tạo tài khoản, bạn sẽ nhận được email giống như hình ảnh dưới đây
![Testapi Reserve](/images/8TestReserveAPi/5.png)




