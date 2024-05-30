---
title : "API"
date : "`r Sys.Date()`"
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

## 1. API tìm chuyến bay

- We will build an API to find flight based on departure date, departure airport. The API return list of flight with details about flights, seats and price information. API call are secured by JWT token. User login to the Cognito Hosted UI to get JWT token to call API. API verified and then allow the requested action to be perform

## 2. API đặt chỗ

- We will build a Reservation API, that fuction of API to reserve flight. API will take passenger details, reservation details and details of the flight as input. Flight ID return from Find flight API call will provide as input to this API. API call are secured by JWT token. Take it like you got it when call API Find Flight


## Nội dung:

1. [**API tìm chuyến bay** API](8.1-apifindflight/)
2. [**API đặt chỗ** API ](8.2-apireserve/)
