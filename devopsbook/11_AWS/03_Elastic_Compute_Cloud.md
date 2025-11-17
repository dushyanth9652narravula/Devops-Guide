# Elastic Compute Cloud (EC2)

## Introduction

- Ec2 stands for Elastic Compute Cloud which is used to create and manage virtual machines in amazon cloud. Ec2 proivdes a web service for provisioning, managing and deprovisioning the virtual machines in amazon cloud.

- When you launch an Ec2 instance, you actually creating a virtual machine running on top of Amazons physical infrastructure.

- Ec2 is elastic in nature which means we can scale it up or down as we want. That means if more users are accessing your application then we can scale that instance (where application is deployed) easily.

- Ec2 can be integrated with other services in AWS such as S3, EFS, EBS very easily.

## EC2 Pricing

- There are actually four types of Ec2 instance in AWS. Those are

  **On Demand Instances** : On Demand Instances is a type of EC2 instance which can be launched at any time. If you want the Compute power at any time amazon provides you that as EC2 service. For this type of instance you need to pay per hour or seconds.

  **Reserved Instances** : AWS provides reserved instances also, which means we can reserve a particular EC2 capacity (or compute power ) for certain period of time. Generally reserved instances comes with more discounts as you are using that instance for long time.

  **Spot Instances** : As we know that AWS infrastructure is very huge. So there might be many unused EC2 capacity (Compute Power). To make these instances gets used, AWS proivides a bidding mechanism where you can bid for an EC2 capacity. If you bid more then you can use that EC2 capacity. But there is one issue, if any other person bids more then you lost your instance and that capacity is reassigned to new customer. (Generally there is a base price for unused EC2 capacity).

  **Dedicated Hosts** : In this type, AWS dedicates entire physical server to you for your use. This would be very costly when compared to other type of EC2 capacity.

## Components of EC2 

- **AMI** : AMI stands for Amazon Machine Image which is a template that contains the information required to launch an EC2 instance including Operating System and other necessary settings. It includes what type of operating system, what application softwares are included, and system configuration also.

- **Instance Type** : When you launch an instance, then instance type determines the hardware of host computer used for that instance. That means instance type determines the CPU, RAM etc.

- **Elastic Block Storage (EBS)** : Elastic Block Storage (EBS) is the default storage system used by Amazon EC2 instance. We use EBS to storage Opearating system, application files and data. But many people think that we get storage from instance type. Actually instance type doesn't decide the storage. We need to configure the storage for Ec2 instance seperately. The default one is EBS. But some instance have default storage, but it would be vanishes when the instances gets stopped or terminated.

- **Tags** : Tag is simple label consisting of customer defined key and an optional value that makes easier to manage, search for, and filter resources.

- **Security Groups** : Security Groups acts as virtual firewalls that controls the traffic for one or more instances.

- **Key-Pair** : Amazon Uses public key crypotography to encrypt and decrypt login information.

## Creation of an EC2 instance

- In order to create an EC2 Instance first login to AWS Management Console and search for EC2 instance. Once you opened EC2 Service, there you can see many sections on left hand side. In there, click on EC2 Instance.

- Once you opened instances tab, just click on launch instances then you can see the Instance creation page.

- At first you have name the EC2 instance. After naming the EC2 instance, now select the AMI that you actually want to use in your application. There are so many AMIs available in AWS. In those some quick start AMIs are free tier eligible. There are AWS Marketplace AMIs which are included with softwares along with OS and those are costly. If you want to learn EC2 Service then select free tier AMI

- Once you selected your AMI, now you have to select your instance type which determines hardware for you instance such as no of CPUs and RAM. As no of CPUs and RAM Size increases, the pricing of instance increases.

- Once you selected your instance type, now you have to create your key-pair, which is used to login to ec2 instance via SSH. Once you clicked on create new key-pair, then name the key-pair and select `.pem` format, so that we can access the instance from git bash (as git bash has ssh service by default). Once you clicked on create button, then a private key gets downloaded to our system which is used to login to the Ec2 instance.

- Once you have created a key-pair, now we have select the volume which is the disk storage for Ec2 instance (which is EBS by default).

- After assigning the disk storage, now we have to assign a security group to the instance which controls the inbound and outbound traffic to the instance. In that security group, you can edit the inbound rules, such as allowing ssh login from your IP only, etc. Like that you edit as many rules as you want.

- Once you assigned the security group to the instance, now click on advanced details and go down, there you can see a option called upload a file. This file is actually used to provision the VM while launching it. Here you can upload a bash script file (if it is linux AMI) or else you can write the scripts in the comment box which gets executed when you launch your instance.


