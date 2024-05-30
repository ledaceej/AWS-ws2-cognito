---
title : "DB find flight"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 6.1 </b> "
---

#### Design Database

- Airport table - stores the details of the Airport with Airport Code as primary key and associated airport details. 
- Flight table - stores the inventory of flights with their schedule, capacity and seat availability.


#### Create table and data
1. We create table by running SQL command below in MySQL Workbench to load 2 table data
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
2. Paste SQL command to MySQL Workbench.
![Config DB](/images/5ConfigDB/15.png)
3. Execute SQL command to create 2 table and see result.
![Config DB](/images/5ConfigDB/16.png)
4. We do by the same way with SQL command below to load data in to 2 table that we created in previous step

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
 Run the SQL command and see the result
![Config DB](/images/5ConfigDB/17.png)
5. Check one table and data.
![Config DB](/images/5ConfigDB/18.png)