# AWS VPC Network Setup and Load Balancing with EC2, MySQL, and Route 53

## Overview

This project demonstrates how to set up an AWS VPC with a load balancer distributing traffic to two web servers hosted on EC2 instances. The architecture also includes a MySQL database in a private subnet. Additionally, **Route 53** is used to transfer a domain from Hostinger to AWS name servers and obtain an SSL certificate for secure web traffic.

## Architecture Diagram

The following architecture was implemented as part of this project:

![Architecture Diagram]
![image](https://github.com/user-attachments/assets/c6fe87b6-6231-45d7-9d02-d4cefaed4e0b)


- **VPC**: Contains public and private subnets.
- **Load Balancer**: Distributes traffic between two EC2 instances in the front-end private subnet.
- **Web App Servers**: Two EC2 instances in the private subnet serving a web application.
- **MySQL Database**: Deployed in the back-end private subnet.
- **NAT Gateway**: Allows outbound internet access for instances in the private subnet.
- **Route 53**: Used for domain name management, transferring the domain from Hostinger to AWS name servers, and obtaining an SSL certificate via AWS Certificate Manager (ACM).

## AWS VPC: Public and Private Subnet Overview

- **VPC**: Set up a custom VPC with public and private subnets.
  - **Public Subnet**: Contains a **NAT Gateway** for outbound traffic, a **Load Balancer**, and an **SSH server** for administrative access.
  - **Private Subnet (Front-End)**: Hosts the EC2 instances (web servers).
  - **Private Subnet (Back-End)**: Hosts the MySQL database.
  - 
## Documentation
A full project report is available in `aws_report.pdf`. 

## Video Presentation
A video presentation demonstration of the VPC setup is available on YouTube:  
[Watch the Video Presentation](https://www.youtube.com/watch?v=ja82c77TEF0&t=1s)
