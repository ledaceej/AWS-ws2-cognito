---
title : "DB tìm chuyến bay"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 6.1 </b> "
---

#### Thiết kế Database

- Bảng Airport  - lưu thông tin của sân bay với airport code là primary key và liên kết các thông tin kahcs của airport. 
- Bảng Flight - Lưu thông tin các chuyến bay với lịch, chỗ ngồi tối đa, chỗ ngồi còn trống


#### Tạo bảng và dữ liệu
1. Ta tạo bảng bằng chạy câu lệnh SQL dưới đây trong MySQL Workbench để tải dữ liệu cho 2 bảng
```
    USE FlightReservationDB;

    CREATE TABLE airport(
        airport_code VARCHAR(10) PRIMARY KEY,
        airport_name VARCHAR(50),
        airport_city VARCHAR(50),
        airport_locale VARCHAR(50)
    );

    CREATE TABLE flight (
        id INT PRIMARY KEY,
        departure_date DATE,
        departure_time TIME,
        departure_airport_code VARCHAR(3),
        arrival_date DATE,
        arrival_time TIME,
        arrival_airport_code VARCHAR(3),
        flight_number VARCHAR(10),
        flight_duration INT,
        ticket_price DOUBLE,
        ticket_currency VARCHAR(3),
        seat_capacity INT,
        seat_available INT,
        CONSTRAINT fk_departure_airport_code FOREIGN KEY (departure_airport_code) REFERENCES airport(airport_code),
        CONSTRAINT fk_arrival_airport_code FOREIGN KEY (arrival_airport_code) REFERENCES airport(airport_code)
    );

 ```
2. Dán câu lệnh SQL vào MySQL Workbench.
![Config DB](/images/5ConfigDB/15.png)
3. Thực thi câu lệnh SQL để tạo 2 bảng và quan sát kết quả.
![Config DB](/images/5ConfigDB/16.png)
4. Chúng ta làm tương tự với câu SQL bên dưới để tải dữ liệu vào trong 2 bảng mà đã tạo ở bước trước

```
    insert into airport(airport_code, airport_name, airport_city, airport_locale) 
    VALUES('LHR', 'London Heathrow Airport', 'London', 'UK');

    insert into airport(airport_code, airport_name, airport_city, airport_locale) 
    VALUES('CDG', 'Charles De Gaulle Airport', 'Paris', 'France');

    insert into airport(airport_code, airport_name, airport_city, airport_locale) 
    VALUES('LAX', 'Los Angeles International Airport', 'Los Angeles', 'USA');

    insert into airport(airport_code, airport_name, airport_city, airport_locale) 
    VALUES('MIA', 'Miami International Airport', 'Miami', 'USA');


    insert into flight(id, departure_date, departure_time, departure_airport_code, arrival_date, arrival_time, arrival_airport_code, flight_number, flight_duration, ticket_price, ticket_currency, seat_capacity, seat_available)
    VALUES(1, '2023-08-01', '10:00', 'MIA', '2023-08-01', '14:00', 'LAX', 'MIA-LAX-001', '01:00', '1000', 'USD', 100, 100);

    insert into flight(id, departure_date, departure_time, departure_airport_code, arrival_date, arrival_time, arrival_airport_code, flight_number, flight_duration, ticket_price, ticket_currency, seat_capacity, seat_available)
    VALUES(2, '2023-08-01', '14:00', 'MIA', '2023-08-01', '14:00', 'LAX', 'MIA-LAX-002', '01:00', '1000', 'USD', 100, 100);

    insert into flight(id, departure_date, departure_time, departure_airport_code, arrival_date, arrival_time, arrival_airport_code, flight_number, flight_duration, ticket_price, ticket_currency, seat_capacity, seat_available)
    VALUES(3, '2023-08-01', '15:00', 'LHR', '2023-08-01', '17:00', 'CDG', 'LHR-CDG-001', '01:00', '1000', 'USD', 100, 100);

    insert into flight(id, departure_date, departure_time, departure_airport_code, arrival_date, arrival_time, arrival_airport_code, flight_number, flight_duration, ticket_price, ticket_currency, seat_capacity, seat_available)
    VALUES(4, '2023-08-01', '17:00', 'LHR', '2023-08-01', '17:00', 'CDG', 'LHR-CDG-002', '01:00', '1000', 'USD', 100, 100);

    insert into flight(id, departure_date, departure_time, departure_airport_code, arrival_date, arrival_time, arrival_airport_code, flight_number, flight_duration, ticket_price, ticket_currency, seat_capacity, seat_available)
    VALUES(5, '2023-08-02', '16:00', 'LHR', '2023-08-02', '16:00', 'CDG', 'LHR-CDG-003', '01:00', '1000', 'USD', 100, 100);

 ```
 Chạy câu lệnh và quan sát kết quả
![Config DB](/images/5ConfigDB/17.png)
5. Kiểm tra một bảng và dữ liệu của nó.
![Config DB](/images/5ConfigDB/18.png)