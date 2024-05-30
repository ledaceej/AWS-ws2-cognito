---
title : "Connect to EC2"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

## Preparation steps

Next we will setting EC2 to connect by RDP from your computer

1. From home console, we select **EC2**.

![ConnectEC2](/images/2connectEC@/1.png)

2. Click to **instances running**.

![ConnectEC2](/images/2connectEC@/2.png)

3. Select instance that prompt in display.

![ConnectEC2](/images/2connectEC@/3.png)


4. Click to **security**, and then click to **Security group** to setting RDP.

![ConnectEC2](/images/2connectEC@/5.png)

5. Chose **inbound rules** then **Edit bound rules**.

![ConnectEC2](/images/2connectEC@/6.png)

6. Add rule

![ConnectEC2](/images/2connectEC@/7.png)

7. In **Type** choose RDP and **Source** select **My IP** and **Save rules**.
 
![ConnectEC2](/images/2connectEC@/8.png)

8. Comeback the place that look like the breadcumbs. And click **Connect**
![ConnectEC2](/images/2connectEC@/9.png)
9. Click to **RDP client** and download **remote desktop file**.


![ConnectEC2](/images/2connectEC@/11.png)
10. Open file that you downloaded .

![ConnectEC2](/images/2connectEC@/12.png)

11. Select **Connect** and **Next** in your prompting display to connect remote EC2, until you have to type password. Then you must go to Secret manager service which is save all secrete like password, API key, DB credentials, and you will go there to take the password of user Administrator to connect EC2.
![ConnectEC2](/images/2connectEC@/13.png)
12. From **home console** **select AWS Secretes Manager** and then click to **Secretes** it will prompt to display like the following image below. Locate the entry named **EC2instancesSecret** and select it.

![ConnectEC2](/images/2connectEC@/14.png)
13. Find section **Secret value** and select **Retrieve secret value**.
![ConnectEC2](/images/2connectEC@/15.png)
14.  Copy the **pass_word**, that is password of user Administrator to connect to EC2.

![ConnectEC2](/images/2connectEC@/16.png)
15.  Login to the instance using **Administrator** as the username. Enter the password that you retrieved in the previous step.

![ConnectEC2](/images/2connectEC@/17.png)
16. You login successfully, you will use it in the next section.
![ConnectEC2](/images/2connectEC@/20.png)






