---
title : "Test API"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 8.1.2 </b> "
---

1. After you write API, lets test it. Firstly, find file **FlightBookingApplication.java** by path **src/main/java/com/airlines/catalog/** to open it
![Testapi Find flight](/images/7TestFindFlightAPI/1.png)
2. Click button triangle
![Testapi Find flight](/images/7TestFindFlightAPI/2.png)
3. Chose **Run 'FlightBookingMain'**
![Testapi Find flight](/images/7TestFindFlightAPI/3.png)
4. Wait about seconds to finish starting application
![Testapi Find flight](/images/7TestFindFlightAPI/4.png)
5. Open **PostMan** application to test API
![Testapi Find flight](/images/7TestFindFlightAPI/5.png)
6. In the input URL, paste CRUL below that I prepair for you to save your time. It includes input parameters for calling API
![Testapi Find flight](/images/7TestFindFlightAPI/7.png)
This is **CURL**
```
curl --location 'localhost:8090/flight?departureDate=2023-08-01&departureAirportCode=LHR&arrivalAirportCode=CDG' \
--header 'Authorization: eyJraWQiOiJLQzh0Zzd0VHcraDJoVXAzeHFUNmJybHV6SUloT2JNZWtoZmc5MVNPd2swPSIsImFsZyI6IlJTMjU2In0.eyJhdF9oYXNoIjoiWUpzYVFjaDNlbGt1R2Y3bW9BT0RtUSIsInN1YiI6ImM1OTVhNDEzLTk5NmQtNGFkNi1hNTFiLTVhNTk3ZjE4MTM0YSIsImVtYWlsX3ZlcmlmaWVkIjp0cnVlLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0xLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMV9QTU9zUlBLM1kiLCJjb2duaXRvOnVzZXJuYW1lIjoibGVkYWNkZXB0cmFpIiwiYXVkIjoiNGk3aWJvYzI0aWpxYnNxNTI5ZmI3cG5kOGwiLCJldmVudF9pZCI6IjI4OTVlNWJjLTE4MWYtNDIyOS1hNGFjLTA3MWE3MWJmYjQxNiIsInRva2VuX3VzZSI6ImlkIiwiYXV0aF90aW1lIjoxNzExNzM5MzA3LCJuYW1lIjoibGUgZHVjIGFuaCIsImV4cCI6MTcxMTc0MjkwNywiaWF0IjoxNzExNzM5MzA3LCJqdGkiOiJkOTgzMzMyNC1mOGJlLTRiZGYtODM5MC1mMThkYmMwZTI3MmEiLCJlbWFpbCI6ImxlZGFjZGVwdHJhaUBnbWFpbC5jb20ifQ.E478H8NzHp1a2nt5MmrF8Qe52grqJ8wUk-55INdlaiT2arQQe8Aj1JeIbt8QSs14KTF5iD4EEoLMkkoqDi4JvCG7IU8BYCb-ygEEd6IazVanqO7acduh8xfWSosY3RCrt3xZSdDUHHXLicCBo8yz0Z1TqAWPfxgN1CV46ErRh_zF05HJ1c77ybqUyR5FVyJEGQDs9XkX0MR9ol6rJTWylK2e448MbsHtQ17xfDvOmS_RSUrN4r7zHVmxK2p_23EQ9C54gTs-GXz478JT9T_uR1JXONmtaLZEi7-lfrpB2mkmLd9MQ5dgJfKFd59fd4bV0IKB3G6t2d0ZMnowjitttw'
```
7. You will prompt to staging like image, it is not done to call API
![Testapi Find flight](/images/7TestFindFlightAPI/8.png)
8. Click to **Headers**, see key **Authorization** is the token like apart stuff of **curl** I mention before. It is my expired JWT token, now you must take new JWT token.
![Testapi Find flight](/images/7TestFindFlightAPI/9.png)
9. Back to **Amazon Cognito** chose section **User pools** and click **TwoAuthen-UserPool**  
![Testapi Find flight](/images/7TestFindFlightAPI/10.png)
10. Click **App integration** 
![Testapi Find flight](/images/7TestFindFlightAPI/12.png)
11. Scroll down in the **App client and analysts** chose **App client**
![Testapi Find flight](/images/7TestFindFlightAPI/13.png)
12. In **Hosted UI** section, click  **View Hosted UI**
![Testapi Find flight](/images/7TestFindFlightAPI/14.png)
13. You will prompt to the new Sign in tab. Fill account information that you create at the previous step, and click **Sign in**
![Testapi Find flight](/images/7TestFindFlightAPI/15.png)
14. Copy URL to the Notedpad 
![Testapi Find flight](/images/7TestFindFlightAPI/16.png)
15. Split **id_token**
![Testapi Find flight](/images/7TestFindFlightAPI/17.png)
16. Copy **id_token**. Token valid in 1 hour, if it expired, you will comeback to the previous image and do it again to take new token
![Testapi Find flight](/images/7TestFindFlightAPI/18.png)
17. Paste it to the value of **Authorization**
![Testapi Find flight](/images/7TestFindFlightAPI/19.png)
17. Now we have all input to call API, next click **Send** and see output 
![Testapi Find flight](/images/7TestFindFlightAPI/20.png)
18. It is information of flight. You call find flight API successfully.
![Testapi Find flight](/images/7TestFindFlightAPI/21.png)

