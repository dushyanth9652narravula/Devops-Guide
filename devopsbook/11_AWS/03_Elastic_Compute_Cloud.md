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


