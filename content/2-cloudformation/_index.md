---
title : "CloudFormation"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

## Cloudformation
1. Download the Cloudformation **cfn-basic-setup.yaml** from this location. This cloudformation will setup all the infrastructure in this workshop 
[DownLoad here](https://ws-assets-prod-iad-r-iad-ed304a55c2ca1aee.s3.us-east-1.amazonaws.com/fa91011f-2da1-4cd9-a3ba-57891dcaa6f5/cfn-basic-setup.yaml )

2. Focus how infras of file .yaml

3. In the console search, type cloudformation and select Cloudformation Service


![Cloudformation](/images/1cloudformation/1x.png)
4. Some region will not alvailable create all resources in cloudformation, so firstly you will change region to **us-east-1**

![Cloudformation](/images/1cloudformation/1.png)
5. Then click **Create stack**. 

![Cloudformation](/images/1cloudformation/2.png)
6. Click setting like instruction in image and chose file **cfn-basic-setup.yaml** that you downloaded. and click **Next**

![Cloudformation](/images/1cloudformation/3.png)

7. Fill the unique name and others settings sets default. Then **Next**
![Cloudformation](/images/1cloudformation/4.png)

8. Acknowledge all the options and click **Submit**
![Cloudformation](/images/1cloudformation/5.png)

9. You will prompt the processing wait about 20 minute to complete processcing.
![Cloudformation](/images/1cloudformation/6.png)

10. Screen when the process finish.
![Cloudformation](/images/1cloudformation/7.png)
