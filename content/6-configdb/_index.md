---
title : "Config DB"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

In this guide, we will you MySQL Workbench to connect to Database instances that created by cloudformation. MySQL Workbench can manage database, query data,..

1. Firstly, we back to the remote computer, Open **MySQL Workbench** 
![Config DB](/images/5ConfigDB/1.png)
2. You will prompt like image
![Config DB](/images/5ConfigDB/2.png)
3. In **Database** section, select **Manage Connections** 
![Config DB](/images/5ConfigDB/3.png)
4. Some information that you have to fill, that can take it from **Secretes manager**.
![Config DB](/images/5ConfigDB/4.png)
5. From home console, go to **Secrete manager** and chose **Secretes** section.
![Config DB](/images/5ConfigDB/5.png)
6. Click **RDSSecreteForApp** 
![Config DB](/images/5ConfigDB/6.png)
7. In the **Secrete value**, then go to **Retrieve secrete value**. Some information you will take from here.
![Config DB](/images/5ConfigDB/7.png)
8. In the remote computer, Click **New** and fill information you take from previous step. This fields are match with information in **Secret value** of the previous image

- **Connection name**, you can be named it with any name
- **Hostname** : **host**
- **Username** : **username**
- **Password** : **password**
![Config DB](/images/5ConfigDB/8.png)
9. Then click Store in Vault, fill your passwork and select **Ok**
![Config DB](/images/5ConfigDB/9.png)
10. **Test connection** of database
![Config DB](/images/5ConfigDB/10.png)
11. Made connection succesfully to database instance.
![Config DB](/images/5ConfigDB/11.png)
12. Next step, we connect to Database to create table and data for your microservice. In **Database** section select **Connect to Database** 
![Config DB](/images/5ConfigDB/12.png)
13. Click **OK**
![Config DB](/images/5ConfigDB/13.png)
14. You will prompt to screen. Next step we will design database, and create data to serve my application
![Config DB](/images/5ConfigDB/14.png)

#### Content

1. [Design DB for API find flight](6.1-DBfindflight/)
2. [Design DB for API reserve](6.2-DBreserve/)


