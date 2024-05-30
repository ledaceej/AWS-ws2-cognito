---
title : "Simple Notification Service"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

In this guide, we will discuss how to create subcription that we use to confirm call api successfully.

1. From home console, select **Simple Notification Service**
![SNS](/images/4SNS/1.png)
2. Select **Topics** section
![SNS](/images/4SNS/2.png)
3. You have 1 topic that create from Cloudformation. then Click to topic link
![SNS](/images/4SNS/3.png)
4. In the **reservation-success** topic, click **Create subcription** 
![SNS](/images/4SNS/4.png)
5. Choose protocol **Email**, **Endpoint** is your email that you want to receive notification. Then click **Create subscription**.
![SNS](/images/4SNS/5.png)
6. Check your recieved email, and click **Confirm subscription** 
![SNS](/images/4SNS/6.png)
7. You will prompt page that inform your subscription is confirmed, you can unsubscribe.
![SNS](/images/4SNS/7.png)
8. You setting successfully SNS topic that recieved email to inform API called successful.
![SNS](/images/4SNS/8.png)


