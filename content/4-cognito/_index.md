---
title : "Setting Cognito"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

## Setting Cognito

In this step, we will set Cognito for creating user,password. Using it to authenticate to connect application that like enterprise application.


1. From home console, select **Cognito** 
![Cognito](/images/3Cognito/1.png)
2. Click to **User pool** and select user pool named **TwoAuthen-UserPool**.
![Cognito](/images/3Cognito/2.png)
3. Select **App integration**
![Cognito](/images/3Cognito/3.png)
4. Scroll down to the bottom, and select **UserPoolClient**
![Cognito](/images/3Cognito/4.png)
5. In the **Hosted UI** section, click to **View Hosted UI**
![Cognito](/images/3Cognito/5.png)
6. You will prompt to new tab like image below. This is first time we go here, so firstly we have to **Sign up**.
![Cognito](/images/3Cognito/6.png)
7. Fill information to create user, that we will use for the following section.
![Cognito](/images/3Cognito/7.png)
8. An email sent, that is final step to create user.
![Cognito](/images/3Cognito/8.png)
9. Fill you code you received and click **Confirm account**.
![Cognito](/images/3Cognito/9.png)
10. Now you will redirected to **localhost:8080** page. Ignore error on the page. We will back later to take access token from URL bar for testing API.
![Cognito](/images/3Cognito/10.png)


