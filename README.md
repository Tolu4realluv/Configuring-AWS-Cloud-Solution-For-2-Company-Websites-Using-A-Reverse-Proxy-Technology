# Configuring-AWS-Cloud-Solution-For-2-Company-Websites-Using-A-Reverse-Proxy-Technology
> NB: This infrastructure setup is not included in the AWS free tier. Therefore, delete all resources created immediately after completing the project. If resources are not deleted, monthly costs may be unexpectedly high. Also, setting up a budget and configuring notifications for when our spending reaches a set limit is highly recommended.

## What is a reverse proxy technology?
A reverse proxy is a server, application, or cloud service that acts as an intermediary for one or more web servers. It intercepts and examines incoming client requests before passing them on to the web server, and then returns the web server's response to the client. 

## Features of a reverse proxy technology?

1. **Intercepts Requests**: A reverse proxy catches requests from a user's browser and relays them to the web server.

2. **Returns Responses**: The reverse proxy gets a response from the web server and sends it back to the user.

3. **Provides Security**: A reverse proxy can shield users from harmful content and prevent malware and ransomware attacks.

4. **Balances Load**: A reverse proxy can spread incoming traffic across multiple servers to avoid overloading any single server.

5. **Monitors Traffic**: A reverse proxy can track and log traffic to web servers, aiding in the detection and prevention of security threats.

6. **Provides Analytics**: A reverse proxy can offer detailed insights into website traffic and usage patterns.

7. **Manages IP Addresses**: A reverse proxy can forward or mask a client's IP address, enhancing privacy and improving traffic routing.

8. **Directs Requests**: A reverse proxy can route requests based on various parameters, such as the user's device, location, or network condition.

In this project, we are building a secure infrastructure inside AWS VPC (Virtual Private Cloud) network for a company (funmi's Ink) that uses WordPress CMS for its main business website, and a Tooling Website for its DevOps team. As part of the company's desire for improved security and performance, a decision has been made to use a reverse proxy technology from NGINX to achieve this.
Cost, Security, and Scalability are the major requirements for this project. Hence, implementing the architecture designed below, ensures that infrastructure for both websites, WordPress and Tooling, is resilient to Web Server's failures, can accommodate increased traffic, and, at the same time, has a reasonable cost.

![](https://github.com/Tolu4realluv/Configuring-AWS-Cloud-Solution-For-2-Company-Websites-Using-A-Reverse-Proxy-Technology/blob/main/AWS-Projects-1.webp)

## Starting off our AWS Cloud Project
A few requirements must be met before we begin:
we must properly configure our AWS account and Organization Unit. [Watch How To Do This Here](https://www.youtube.com/watch?v=9PQYCc_20-Q)

1. We Created an [AWS Master account](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all). (Also known as Root Account)
*Within the Root account, we created a sub-account and named it DevOps. (we used another email address to complete this)
*Within the Root account, we created an AWS Organization Unit (OU). and named it Dev. (We will launch Dev resources in there)
*We moved the DevOps account into the Dev OU.
*We logged into the newly created AWS account using the new email address.

2. We Created a free domain name for our company at Freenom domain registrar [here](https://www.freenom.com/en/index.html?lang=en).
3. We Created a hosted zone in AWS and mapped it to our free domain from Freenom. [Watch how to do that here](https://www.youtube.com/watch?v=IjcHp94Hq8A)

## Setting Up a Virtual Private Network (VPC)












