---
title : "DB Reserve"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 6.2 </b> "
---

#### Design Database

- Passenger table - to hold pasenger's personal information
- Reservation table - to hold the flight reservations detail


#### Create table and data
1. Create the tables required for the reservation API.
```
CREATE TABLE passenger (
    passenger_id INT NOT NULL AUTO_INCREMENT,
    adult BOOLEAN NOT NULL,
    gender VARCHAR(10) NOT NULL,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    PRIMARY KEY (passenger_id)
);

CREATE TABLE reservation (
    booking_reference BIGINT NOT NULL AUTO_INCREMENT,
    passenger_id INT NOT NULL,
    flight_id INT NOT NULL,
    reservation_date DATE NOT NULL,
    reservation_time TIME NOT NULL,
    reservation_status VARCHAR(20) NOT NULL,
    travel_class VARCHAR(20) NOT NULL,
    ticket_price DECIMAL(10,2) NOT NULL,
    currency_code VARCHAR(3) NOT NULL,
    payment_status VARCHAR(20) NOT NULL,
    payment_mode VARCHAR(20) NOT NULL,
    contact_number VARCHAR(20) NOT NULL,
    contact_email VARCHAR(50) NOT NULL,
    PRIMARY KEY (booking_reference),
    FOREIGN KEY (passenger_id) REFERENCES passenger(passenger_id),
    FOREIGN KEY (flight_id) REFERENCES flight(id)
);
 ```
 2. Paste SQL command to MySQL Workbench and execute command, then take result.
![Config DB](/images/5ConfigDB/19.png)

