---
title : "API"
date : "`r Sys.Date()`"
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

## 1. Find Flight API

- Chúng ta sẽ dựng một API để tìm chuyến bay dựa trên ngày đến và ngày đi. API sẽ trả về một danh sách các chuyến bay với chi tiết về chuyến bay, thông tin về chỗ ngồi, giá. API được bảo về bởi JWT token. Người dùng đăng nhập tới Cognito Hosted UI để lấy JWT token để gọi API. API được xác thực và sẽ được thực thi.

## 2. Reservation API

- Chúng ta dựng một API đặt chuyến bay, API sẽ lấy thông tin hành khách, chi tiết thông tin đặt chỗ và thông tin của chuyến bay làm đầu ra của API. Flight ID sẽ trả về từ API tìm chuyến bay sẽ cung cấp như một đầu vào của API. Gọi API sẽ được bảo về bởi JWT token. Lấy nó giống như chúng ta lấy nó khi gọi API tìm chuyến bay.


## Content:

1. [**Find Flight** API](8.1-apifindflight/)
2. [**Reservation** API ](8.2-apireserve/)
