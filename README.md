# AWS Review Session 2

## Index

**1. AWS Virtual Private Cloud (VPC)**

1.1. AWS VPC 

1.2. AWS VPC IP Addressing

1.3. Segmenting networks inside a VPC

1.4. AWS Subnets

1.5. Internet Gateway

1.6. Elastic IP Address

1.7. NAT Gateway

1.8. Shared VPC

1.9.vSecurity Groups

1.10. Network Access Control Lists (NACLs)

1.11.VPC Endpoints – Interface and Endpoint

1.12. VPC Peering

**2. AWS Route 53 (DNS)**

**3. AWS Direct Connect**

3.1. Use AWS Direct Connect to securely link your on-premise environment to AWS

3.2. How to add redundancy to my dedicated circuits?

3.3. How to access my VPCs or AWS Public Services over my DX?

3.4. How to connect to multiple AWS Regions/Accounts over DX?

**4. AWS Transit Gateway**

**5. AWS Security Groups and Network Access Control Lists (NACLs)**

**6. AWS Global Accelerator**

**7. AWS Storage Gateway**

## 1. AWS Virtual Private Cloud (VPC)

### 1.1. AWS VPC 

Provision a Logically Isolated Section of the AWS Cloud

• Control your virtual networking environment

• Subnets

• Route tables

• Security Groups

• Network ACLs

• Control if and how your instances access the internet

• Connect to your on-premises network via VPN or Direct Connect

The following diagram shows an example VPC. The VPC has one subnet in each of the Availability Zones in the Region, EC2 instances in each subnet, and an internet gateway to allow communication between the resources in your VPC and the internet

![image](https://github.com/user-attachments/assets/de67648e-f391-4bd4-a342-a773cd8baae2)

https://docs.aws.amazon.com/en_us/vpc/latest/userguide/what-is-amazon-vpc.html

Provision a Logically Isolated Section of the AWS Cloud

![image](https://github.com/user-attachments/assets/404e9d03-3db8-41fb-8b6e-ece3a8511db8)

Here is another example of VPC for web and database servers

This example demonstrates how to create a VPC that you can use for a two-tier architecture in a production environment

To improve resiliency, you deploy the servers in two Availability Zones

![image](https://github.com/user-attachments/assets/ebfceff2-5b57-4151-9e7d-5e420d117a9f)

https://docs.aws.amazon.com/en_us/vpc/latest/userguide/vpc-example-web-database-servers.html

The VPC has public subnets and private subnets in two Availability Zones

The web servers run in the public subnets and receive traffic from clients through a load balancer

The security group for the web servers allows traffic from the load balancer

The database servers run in the private subnets and receive traffic from the web servers

The security group for the database servers allows traffic from the web servers

The database servers can connect to Amazon S3 by using a gateway VPC endpoint

### 1.2. AWS VPC IP Addressing



### 1.3. Segmenting networks inside a VPC



### 1.4. AWS Subnets

Direct traffic out of Subnets



### 1.5. Internet Gateway

Connect VPC to the internet



### 1.6. Elastic IP Address

IP Addresses for your instances



### 1.7. NAT Gateway

Outbound only Internet access


### 1.8. Shared VPC

One account using another’s VPC



### 1.9. Security Groups

Filtering Traffic to Instances


### 1.10. Network Access Control Lists (NACLs)

Filtering Traffic at Subnet Level



### 1.11. VPC Endpoints – Interface and Endpoint

Connect Privately to Public AWS Services

### 1.12. VPC Peering

Connecting directly to other VPCs

![image](https://github.com/user-attachments/assets/fa3b8cf2-6066-4901-8371-463668791bff)

VPC Peering

• Scalable and high available

• Inter-account peering

• Same or different AWS Regions

• Bi-directional traffic

• Remote Security groups can be referenced

• Routing policy with Route Tables; not all subnets need to connect to each other

• No transitive routing, requires full-mesh to interconnect multiple VPCs

• No support for overlapping IP addresses

## 2. AWS Route 53 (DNS)

### 2.1. A reliable and cost-effective way to route end users to Internet applications

Connects user requests to infrastructure running in AWS

Highly available and scalable cloud Domain Name System (DNS) web service

![image](https://github.com/user-attachments/assets/4373e9cf-b902-4849-94d4-c35c05b96f70)

AWS Route 53 Traffic Flow makes it easy to set up sophisticated routing logic for your applications

Using a global anycast network of DNS servers around the world, AWS Route 53 is designed to automatically route your users to the optimal location depending on network conditions

### 2.2. Domain Names to IP Address

![image](https://github.com/user-attachments/assets/4129737e-62bf-4e65-aa13-fdc181f0f4d8)

• AWS DNS service

• Domain Registration

• Domain name resolution

• 100% availability SLA

• Health Checks

• DNS Failover

• Latency Based Routing

• Geo Based Routing

• Weighted Round Robin

• Private DNS for VPC

## 3. AWS Direct Connect

### 3.1. Use AWS Direct Connect to securely link your on-premise environment to AWS


### 3.2. How to add redundancy to my dedicated circuits?



### 3.3. How to access my VPCs or AWS Public Services over my DX?



### 3.4. How to connect to multiple AWS Regions/Accounts over DX?


## 4. AWS Transit Gateway


## 5. AWS Security Groups and NACLs


## 6. AWS Global Accelerator


## 7. AWS Storage Gateway












