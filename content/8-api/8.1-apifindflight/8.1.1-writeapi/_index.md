---
title : "Write API"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 8.1.1 </b> "
---

## Write API
1. You will create model classes to work with **airport** and **flight** table.

- Open **Airport.java** add the following code
```
package com.airlines.catalog.model;

import lombok.Getter;
import lombok.Setter;
import lombok.experimental.Accessors;
import lombok.NoArgsConstructor;
import javax.persistence.*;

/* Create an Entity class Airport mapped to table airport with following 4 attributes:
airportCode as id, airportName, airportCity and airportLocale.
They should be mapped to database columns with _ as separator.*/

@Entity
@Table(name = "airport")
@Accessors(chain = true)
@NoArgsConstructor
public class Airport {
    public String getAirportCode() {
        return airportCode;
    }

    public void setAirportCode(String airportCode) {
        this.airportCode = airportCode;
    }

    public String getAirportName() {
        return airportName;
    }

    public void setAirportName(String airportName) {
        this.airportName = airportName;
    }

    public String getAirportCity() {
        return airportCity;
    }

    public void setAirportCity(String airportCity) {
        this.airportCity = airportCity;
    }

    public String getAirportLocale() {
        return airportLocale;
    }

    public void setAirportLocale(String airportLocale) {
        this.airportLocale = airportLocale;
    }

    @Id
    @Column(name = "airport_code")
    private String airportCode;
    @Column(name = "airport_name")
    private String airportName;
    @Column(name = "airport_city")
    private String airportCity;
    @Column(name = "airport_locale")
    private String airportLocale;
}
```
- Open **Flight.java** add the following code
```

```
2. Create Data Transfer Object(DTO) to combine the information from flight and airport tables 
- Open **FlightDetails.java** add the following code
```
package com.airlines.catalog.model;

import lombok.Getter;
import lombok.Setter;
import lombok.experimental.Accessors;
import lombok.NoArgsConstructor;
import javax.persistence.*;

@Entity
@Table(name = "flight")
@Accessors(chain = true)
@NoArgsConstructor
public class Flight {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    @Column(name = "id")
    private int id;

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getDepartureDate() {
        return departureDate;
    }

    public void setDepartureDate(String departureDate) {
        this.departureDate = departureDate;
    }

    public String getDepartureTime() {
        return departureTime;
    }

    public void setDepartureTime(String departureTime) {
        this.departureTime = departureTime;
    }

    public String getDepartureAirportCode() {
        return departureAirportCode;
    }

    public void setDepartureAirportCode(String departureAirportCode) {
        this.departureAirportCode = departureAirportCode;
    }

    public String getArrivalDate() {
        return arrivalDate;
    }

    public void setArrivalDate(String arrivalDate) {
        this.arrivalDate = arrivalDate;
    }

    public String getArrivalTime() {
        return arrivalTime;
    }

    public void setArrivalTime(String arrivalTime) {
        this.arrivalTime = arrivalTime;
    }

    public String getArrivalAirportCode() {
        return arrivalAirportCode;
    }

    public void setArrivalAirportCode(String arrivalAirportCode) {
        this.arrivalAirportCode = arrivalAirportCode;
    }

    public String getFlightNumber() {
        return flightNumber;
    }

    public void setFlightNumber(String flightNumber) {
        this.flightNumber = flightNumber;
    }

    public String getFlightDuration() {
        return flightDuration;
    }

    public void setFlightDuration(String flightDuration) {
        this.flightDuration = flightDuration;
    }

    public double getTicketPrice() {
        return ticketPrice;
    }

    public void setTicketPrice(double ticketPrice) {
        this.ticketPrice = ticketPrice;
    }

    public String getTicketCurrency() {
        return ticketCurrency;
    }

    public void setTicketCurrency(String ticketCurrency) {
        this.ticketCurrency = ticketCurrency;
    }

    public int getSeatCapacity() {
        return seatCapacity;
    }

    public void setSeatCapacity(int seatCapacity) {
        this.seatCapacity = seatCapacity;
    }

    public int getSeatAvailable() {
        return seatAvailable;
    }

    public void setSeatAvailable(int seatAvailable) {
        this.seatAvailable = seatAvailable;
    }

    @Column(name = "departure_date")
    private String departureDate;
    @Column(name = "departure_time")
    private String departureTime;
    @Column(name = "departure_airport_code")
    private String departureAirportCode;
    @Column(name = "arrival_date")
    private String arrivalDate;
    @Column(name = "arrival_time")
    private String arrivalTime;
    @Column(name = "arrival_airport_code")
    private String arrivalAirportCode;
    @Column(name = "flight_number")
    private String flightNumber;
    @Column(name = "flight_duration")
    private String flightDuration;
    @Column(name = "ticket_price")
    private double ticketPrice;
    @Column(name = "ticket_currency")
    private String ticketCurrency;
    @Column(name = "seat_capacity")
    private int seatCapacity;
    @Column(name = "seat_available")
    private int seatAvailable;

    @Override
    public String toString() {
        return "Flight{" +
                "id=" + id +
                ", departureDate='" + departureDate + '\'' +
                ", departureTime='" + departureTime + '\'' +
                ", departureAirportCode='" + departureAirportCode + '\'' +
                ", arrivalDate='" + arrivalDate + '\'' +
                ", arrivalTime='" + arrivalTime + '\'' +
                ", arrivalAirportCode='" + arrivalAirportCode + '\'' +
                ", flightNumber='" + flightNumber + '\'' +
                ", flightDuration='" + flightDuration + '\'' +
                ", ticketPrice=" + ticketPrice +
                ", ticketCurrency='" + ticketCurrency + '\'' +
                ", seatCapacity=" + seatCapacity +
                ", seatAvailable=" + seatAvailable +
                '}';
    }
    public String toJson() {
        return "{" +
                "\"id\":" + id +
                ", \"departureDate\":\"" + departureDate + '\"' +
                ", \"departureTime\":\"" + departureTime + '\"' +
                ", \"departureAirportCode\":\"" + departureAirportCode + '\"' +
                ", \"arrivalDate\":\"" + arrivalDate + '\"' +
                ", \"arrivalTime\":\"" + arrivalTime + '\"' +
                ", \"arrivalAirportCode\":\"" + arrivalAirportCode + '\"' +
                ", \"flightNumber\":\"" + flightNumber + '\"' +
                ", \"flightDuration\":\"" + flightDuration + '\"' +
                ", \"ticketPrice\":" + ticketPrice +
                ", \"ticketCurrency\":\"" + ticketCurrency + '\"' +
                ", \"seatCapacity\":" + seatCapacity +
                ", \"seatAvailable\":" + seatAvailable +
                '}';
    }
}
```
3. Build JPA Repository Interface to access data from MySQL tables
- Open **AirportRepository.java** add the following code
```
package com.airlines.catalog.repository;

import com.airlines.catalog.model.Airport;
import org.springframework.stereotype.Repository;
import org.springframework.data.jpa.repository.JpaRepository;

@Repository
public interface AirportRepository extends JpaRepository<Airport, String> {
    Airport findByAirportCode(String airportCode);
}
```
- Open **FlightRepository.java** add the following code
```
package com.airlines.catalog.repository;

import com.airlines.catalog.model.Flight;
import org.springframework.stereotype.Repository;
import org.springframework.data.jpa.repository.JpaRepository;

@Repository
public interface FlightRepository extends JpaRepository<Flight, Integer> {
    Iterable<Flight> findByDepartureDateAndDepartureAirportCodeAndArrivalAirportCode(String departureDate, String departureAirportCode, String arrivalAirportCode);
    Flight findById(int id);
}
```
4. Build a Configuration Class to dynamically configure database credentials from AWS Secrets Manager.
- Open **DataSourceConfig.java** add the following code
```
package com.airlines.catalog.config;

import com.fasterxml.jackson.core.JsonProcessingException;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import software.amazon.awssdk.regions.Region;
import software.amazon.awssdk.services.secretsmanager.SecretsManagerClient;
import software.amazon.awssdk.services.secretsmanager.model.GetSecretValueRequest;
import software.amazon.awssdk.services.secretsmanager.model.GetSecretValueResponse;
import software.amazon.awssdk.services.secretsmanager.model.SecretsManagerException;

import org.springframework.boot.jdbc.DataSourceBuilder;
import com.fasterxml.jackson.core.JsonParser;
import com.fasterxml.jackson.databind.JsonNode;
import com.fasterxml.jackson.databind.ObjectMapper;
import javax.sql.DataSource;

/*Create public class DataSourceConfig and 2 member variables awsRegion and secretName.
Autowire these variables with aws.region and secretmanager.key from application.properties file.
*/
@Configuration
public class DataSourceConfig {

    @Value("${aws.region}")
    private String awsRegion;

    @Value("${secretmanager.key}")
    private String secretName;

    /* Create a private getSecret method that connects to AWS Secrets Manager and gets the secret string using
    member variables awsRegion and secretName. Catch and throw Secret Manager exceptions  */
    private String getSecret() {
        Region region = Region.of(awsRegion);
        SecretsManagerClient client = SecretsManagerClient.builder()
                .region(region)
                .build();

        GetSecretValueRequest valueRequest = GetSecretValueRequest.builder()
                .secretId(secretName)
                .build();

        GetSecretValueResponse valueResponse = client.getSecretValue(valueRequest);
        return valueResponse.secretString();
    }

    /* Create a method getDataSource to build the datasource object.
   Call the getSecret function. Parse  the returned JSON string to extract host, port, db,
   username and password. Then configure the mysql url, username and password of the datasource object.
   Return the datasource object. Throw any Json Processing exception.
   */
    @Bean
    public DataSource getDataSource() throws JsonProcessingException {
        DataSourceBuilder<?> dataSourceBuilder = DataSourceBuilder.create();
        String secret = getSecret();
        ObjectMapper objectMapper = new ObjectMapper();
        objectMapper.configure(JsonParser.Feature.ALLOW_COMMENTS, true);
        JsonNode jsonNode = objectMapper.readTree(secret);
        String host = jsonNode.get("host").asText();
        int port = jsonNode.get("port").asInt();
        String db = jsonNode.get("db").asText();
        String username = jsonNode.get("username").asText();
        String password = jsonNode.get("password").asText();
        dataSourceBuilder.url("jdbc:mysql://" + host + ":" + port + "/" + db);
        dataSourceBuilder.username(username);
        dataSourceBuilder.password(password);
        return dataSourceBuilder.build();
    }

}
```
5. Build the service class that will fetch the data from flight table to get available flights based on input parameters
- Open **FlightDetailsService.java** add the following code
```
package com.airlines.catalog.service;

import com.airlines.catalog.dto.FlightDetails;
import com.airlines.catalog.model.Airport;
import com.airlines.catalog.model.Flight;
import com.airlines.catalog.repository.AirportRepository;
import com.airlines.catalog.repository.FlightRepository;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;
import java.util.ArrayList;
import java.util.List;

/* Create FlightDetailsService class */
@Service
public class FlightDetailsService {

    @Autowired
    FlightRepository flightRepository;

    @Autowired
    AirportRepository airportRepository;

    /* Create private method populateFlightDetails method which takes flight, arrival airport and departure airport
   as input parameters and returns flightDetails object. */
    private FlightDetails populateFlightDetails(Flight flight, Airport arrivalAirport, Airport departureAirport) {
        /* Match and Assign all the attributes from flight, arrivalAirport and departureAirport object
    to flightDetails object. */
        FlightDetails flightDetails = new FlightDetails();
        flightDetails.setFlightId(flight.getId());
        flightDetails.setDepartureDate(flight.getDepartureDate());
        flightDetails.setDepartureTime(flight.getDepartureTime());
        flightDetails.setArrivalDate(flight.getArrivalDate());
        flightDetails.setArrivalTime(flight.getArrivalTime());
        flightDetails.setArrivalAirportCode(arrivalAirport.getAirportCode());
        flightDetails.setArrivalAirportName(arrivalAirport.getAirportName());
        flightDetails.setArrivalAirportCity(arrivalAirport.getAirportCity());
        flightDetails.setArrivalAirportLocale(arrivalAirport.getAirportLocale());
        flightDetails.setDepartureAirportCode(departureAirport.getAirportCode());
        flightDetails.setDepartureAirportName(departureAirport.getAirportName());
        flightDetails.setDepartureAirportCity(departureAirport.getAirportCity());
        flightDetails.setDepartureAirportLocale(departureAirport.getAirportLocale());
        flightDetails.setFlightDuration(flight.getFlightDuration());
        flightDetails.setTicketPrice(flight.getTicketPrice());
        flightDetails.setTicketCurrency(flight.getTicketCurrency());
        flightDetails.setSeatAvailable(flight.getSeatAvailable());
        flightDetails.setFlightNumber(flight.getFlightNumber());
        return flightDetails;
    }
    public List<FlightDetails> findFlights(String departureDate, String departureAirportCode,
                                           String arrivalAirportCode, FlightRepository flightRepository,
                                           AirportRepository airportRepository) {
        
        Iterable<Flight> flights = flightRepository.findByDepartureDateAndDepartureAirportCodeAndArrivalAirportCode(departureDate, departureAirportCode, arrivalAirportCode);
        
        List<FlightDetails> flightDetailsList = new ArrayList<>();
        for (Flight flight : flights) {
            Airport departureAirport = airportRepository.findByAirportCode(flight.getDepartureAirportCode());
            Airport arrivalAirport = airportRepository.findByAirportCode(flight.getArrivalAirportCode());
            FlightDetails flightDetails = populateFlightDetails(flight, arrivalAirport, departureAirport);
            flightDetailsList.add(flightDetails);
        }
        return flightDetailsList;
    }

}
```
6. Build the RSA Key provider class to get the Cognito public key. This will be used to verify the JWT Token later.
- Open **AwsCognitoRSAKeyProvider.java** add the following code
```
package com.airlines.catalog.controller;

import com.auth0.jwk.JwkException;
import com.auth0.jwk.JwkProvider;
import com.auth0.jwk.JwkProviderBuilder;
import com.auth0.jwt.interfaces.RSAKeyProvider;
import java.net.MalformedURLException;
import java.net.URL;
import java.security.interfaces.RSAPrivateKey;
import java.security.interfaces.RSAPublicKey;

/* create a class to implement methods for public key verification.
URL is provided as input
Add other mandatory methods to implement the interface. Handle all the exceptions.
*/
public class AwsCognitoRSAKeyProvider implements RSAKeyProvider {

    private final JwkProvider provider;

    public AwsCognitoRSAKeyProvider(String url) throws MalformedURLException {
        provider = new JwkProviderBuilder(new URL(url)).build();
    }

    @Override
    public RSAPublicKey getPublicKeyById(String kid) {
        try {
            return (RSAPublicKey) provider.get(kid).getPublicKey();
        } catch (JwkException e) {
            e.printStackTrace();
        }
        return null;
    }

    @Override
    public RSAPrivateKey getPrivateKey() {
        return null;
    }

    @Override
    public String getPrivateKeyId() {
        return null;
    }
}
```
7. Build the exception handler to handle Cognito authentication errors and define custom application messages for few commonly encountered exceptions.
- Open **AuthenticationException.java** add the following code
```
package com.airlines.catalog.exception;

import com.auth0.jwt.exceptions.InvalidClaimException;
import com.auth0.jwt.exceptions.JWTDecodeException;
import com.auth0.jwt.exceptions.TokenExpiredException;

import java.net.CacheRequest;
import java.net.MalformedURLException;

import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import lombok.Getter;
/*Create a public class AuthenticationException that extends Runtime Exception with member variable
response entity and constructor with Exception as input parameter.
Check for different types of JWT exceptions
Store the message in member variable response entity.
*/
@Getter
public class AuthenticationException extends RuntimeException {

    private ResponseEntity responseEntity;

    public AuthenticationException(Exception e) {
        if (e instanceof JWTDecodeException) {
            responseEntity = new ResponseEntity<>("Invalid Token", HttpStatus.UNAUTHORIZED);
        } else if (e instanceof TokenExpiredException) {
            responseEntity = new ResponseEntity<>("Token Expired", HttpStatus.UNAUTHORIZED);
        } else if (e instanceof InvalidClaimException) {
            responseEntity = new ResponseEntity<>("Invalid Claim", HttpStatus.UNAUTHORIZED);
        } else if (e instanceof MalformedURLException) {
            responseEntity = new ResponseEntity<>("Invalid URL", HttpStatus.UNAUTHORIZED);
        }
    }


}
```
8. Build the controller class for exposing the "getFlightDetails" API CodeWhisperer prompts to build the API Controller:
- Open **FlightReservation.java** add the following code
```
package com.airlines.catalog.controller;

import java.nio.channels.ScatteringByteChannel;
import java.util.List;
import com.airlines.catalog.dto.FlightDetails;
import com.airlines.catalog.exception.AuthenticationException;
import com.airlines.catalog.repository.AirportRepository;
import com.airlines.catalog.repository.FlightRepository;
import com.airlines.catalog.service.FlightDetailsService;
import com.auth0.jwt.JWT;
import com.auth0.jwt.JWTVerifier;
import com.auth0.jwt.algorithms.Algorithm;
import com.auth0.jwt.interfaces.DecodedJWT;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestHeader;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.RestController;
import com.airlines.catalog.repository.PassengerRepository;
import com.airlines.catalog.repository.ReservationRepository;
import com.airlines.catalog.service.FlightBooking;
import com.airlines.catalog.dto.ReservationDetails;
import com.airlines.catalog.exception.FlightNotFoundException;
import com.airlines.catalog.exception.RequestedSeatsNotAvailable;
import com.airlines.catalog.model.Passenger;
import com.airlines.catalog.model.Reservation;
import org.springframework.web.bind.annotation.*;
import software.amazon.awssdk.regions.Region;
import javax.validation.Valid;



@RestController
public class FlightReservation {
    @Autowired
    FlightRepository flightresultsRepository;
    @Autowired
    AirportRepository airportresultsRepository;
    @Autowired
    FlightDetailsService FlightDetailsService;

    @Autowired
    PassengerRepository passengerRepository;
    @Autowired
    ReservationRepository reservationRepository;
    @Autowired
    FlightBooking flightBooking;

    @Value("${cognito.userpool.id}")
    private String cognitoUserPoolId;
    @Value("${aws.region}")
    private String awsRegion;
    @Value("${sns.arn}")
    private String snsTopicArn;

    /* Create a private method verifyToken to verify JWT token with input parameters as
    Cognito user pool id, AWS region and token string. Function returns a Boolean.
    Construct the Cognito well known url and then verify the token using RSA Algorithm.
    catch all Exception throw new authenticationException.*/
    private Boolean verifyToken(String cognitoUserPoolId, String awsRegion, String token) throws AuthenticationException {
        try {
            System.out.println("token=" + token);

            String cognitoWellKnownUrl = "https://"+ cognitoUserPoolId + "/.well-known/jwks.json";
            Algorithm algorithm = Algorithm.RSA256(new AwsCognitoRSAKeyProvider(cognitoWellKnownUrl));
            JWTVerifier verifier = JWT.require(algorithm).build();
            DecodedJWT decodedJWT = verifier.verify(token);
            return true;
        } catch (Exception e) {
            throw new AuthenticationException(e);
        }
    }

    /* Create a rest controller getFlightDetails to get flight details with HTTP GET Method ,
   /flight path and request parameters as departure date, departure airport code and arrival airport code
   JWT Token in the Authorization Header.
   Rest controller returns a ResponseEntity of string.
   */
    @GetMapping("/flight")
    public ResponseEntity<String> getFlightDetails(@RequestParam("departureDate") String departureDate,
                                                   @RequestParam("departureAirportCode") String departureAirportCode,
                                                   @RequestParam("arrivalAirportCode") String arrivalAirportCode,
                                                   @RequestHeader("Authorization") String authorization) throws AuthenticationException {
        /* Call verifyToken method, catch authentication exception and return the responseEntity
    if token is valid and call the findFlights method in FlightDetailsService class
    with input parameters  departure date, departure airport code,
    arrival airport code, flightResultsRepository and airportResultsRepository.
    If flights are found return the list of flights otherwise return "No flights found".
    If authentication failed the return "Authentication failed" and HTTP status of forbidden
    */
        try {
            if (verifyToken(cognitoUserPoolId, awsRegion, authorization)) {
                List<FlightDetails> flights = FlightDetailsService.findFlights(departureDate, departureAirportCode, arrivalAirportCode, flightresultsRepository, airportresultsRepository);
                if (flights.size() > 0) {
                    return new ResponseEntity<>(flights.toString(), HttpStatus.OK);
                } else {
                    return new ResponseEntity<>("No flights found", HttpStatus.OK);
                }
            } else {
                return new ResponseEntity<>("Authentication failed", HttpStatus.FORBIDDEN);
            }
        } catch (AuthenticationException e) {
            return e.getResponseEntity();
        }

    }

    /* Create a rest controller bookFlight to get flight details with HTTP POST Method ,
/reserve path and request body reservationDetails. Rest controller returns a ResponseEntity of string.
Authorization token is passed in the header of the request.
*/
    @PostMapping("/reserve")
    public ResponseEntity<String> bookFlight(@RequestBody @Valid ReservationDetails reservationDetails,
                                             @RequestHeader("Authorization") String authorization)
            throws AuthenticationException, FlightNotFoundException, RequestedSeatsNotAvailable {
        ResponseEntity<String> responseEntity = null;
        /*validate the token by calling verifyToken method in a try catch block.
Catch authenticationExceptionHandler exception return the response entity object
from the exception object*/

        try {
            if (verifyToken(cognitoUserPoolId, awsRegion, authorization)) {
                /* create passenger object assign first name, last name and gender of passenger object from reservationDetails object */
                Passenger passenger = new Passenger();
                passenger.setFirstName(reservationDetails.getFirstName());
                passenger.setLastName(reservationDetails.getLastName());
                passenger.setGender(reservationDetails.getGender());
                //Check the age from reservationDetails object and populate adult field
                if (reservationDetails.getAge() >= 18) {
                    passenger.setAdult(true);
                }
                /* create reservation object Assign flightId, travelClass, ticketPrice, currencyCode,contactEmail,
                 contactNumber, reservationStatus, paymentStatus, paymentMode */
                Reservation reservation = new Reservation();
                reservation.setFlightId(reservationDetails.getFlightId());
                reservation.setTravelClass(reservationDetails.getTravelClass());
                reservation.setTicketPrice(reservationDetails.getTicketPrice());
                reservation.setCurrencyCode(reservationDetails.getCurrencyCode());
                reservation.setContactEmail(reservationDetails.getContactEmail());
                reservation.setContactNumber(reservationDetails.getContactNumber());
                reservation.setReservationStatus("Pending");
                reservation.setPaymentStatus("Pending");
                reservation.setPaymentMode("Cash");
                /* set the date reservation date in yyyy-MM-dd format and
                reservation time in HH:mm:ss format for current date and time*/
                reservation.setReservationDate(java.time.LocalDate.now().toString());
                reservation.setReservationTime(java.time.LocalTime.now().toString());

                Boolean result;
                try {
                    int noOfPassengers = 1;
                    Region region = Region.of(awsRegion);
                    result = flightBooking.reserveFlight(passenger, reservation, passengerRepository,
                            reservationRepository, flightresultsRepository, noOfPassengers, snsTopicArn, region);
                }
                catch (FlightNotFoundException e) {
                    return e.getResponseEntity();
                }
                catch (RequestedSeatsNotAvailable e) {
                    return e.getResponseEntity();
                }
                /* check if the reservation is successful
                 return response entity object with HTTP status of ok and
                message "reservation made successfully" appending the booking Reference
                if the reservation is not successful
                return response entity object with HTTP status of bad request */
                if (result) {
                    responseEntity = new ResponseEntity<>("Reservation made successfully. Booking Reference: " + reservation.getBookingReference(), HttpStatus.OK);
                }
                else {
                    responseEntity = new ResponseEntity<>("Reservation failed", HttpStatus.BAD_REQUEST);
                }

            }
        } catch (AuthenticationException e) {
            responseEntity = e.getResponseEntity();
        }
        return responseEntity;
    }
}
```
