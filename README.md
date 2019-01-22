AWS Certified Solutions Architect  Associate -  Notes
=====================================
- [VPC](#vpc)
    - [What is a VPC?](#what-is-a-vpc)
    - [VPC - AWS Definition](#vpc-aws-definition)
    - [What can you do with a VPC?](#what-can-you-do-with-a-vpc)
    - [Default VPC vs Custom VPC](#default-vpc-vs-custom-vpc)
    - [NAT Instances vs NAT Gateways](#nat-instances-vs-nat-gateways)
    - [VPC Flow Logs](#vpc-flow-logs)
    - [VPC Peering](#vpc-peering)
    - [VPC Access types](#vpc-access-types)
        - [Direct Connect](#direct-connect)
        - [AWS VPN CloudHub](#aws-vpn-cloudhub)
    - [VPC Exam Tips](#vpc-exam-tips)
    - [VPC Warnings](#vpc-warnings)
    - [VPC Limits](#vpc-limits)
- [EC2](#ec2)
    - [EC2 On-demand](#ec2-on-demand)
    - [EC2 Reserved Instance](#ec2-reserved-instance)
    - [Spot Instance](#spot-instances)
    - [Dedicated Instances](#dedicated-instances)
    - [High Performance Computing (HPC)](#high-performance-computing-hpc)
    - [Security Grups](#security-groups)
    - [Placement Groups](#placement-groups)
    - [EC2 Exam Tips](#ec2-exam-tips)
    - [Volume vs Snapshot Exam Tips](#volume-vs-snapshot-exam-tips)
    - [Warnings](#ec2-warnings)
    - [Limits](#ec2-limits)
- [Load Balancer](#load-balancer)
    - [Classic Load Balancer (CLB)](#classic-load-balancer-clb)
    - [Application Load Balancer (ALB)](#application-load-balancer-alb)
    - [Warnings](#lb-warnings)
- [Auto Scaling](#auto-scaling)
- [Elastic Block Storage (EBS)](#elastic-block-storage-ebs)
    - [General Purpose SSD (GP2)](#general-purpose-ssd-gp2)
    - [Provisioned IOPS SSD (IO1)](#provisioned-iops-ssd-io1)
    - [Throughput Optimized HDD (ST1)](#throughput-optimized-hdd-st1)
    - [Cold HDD (SC1)](#cold-hdd-sc1)
    - [Magnetic (Standard)](#magnetic-standard) 
    - [Increasing IOPS Performance](#increasing-iops-performance)
    - [EBS-optimized instances](#ebs-optimized-instances)
    - [EBS Snapshots Characteristics](#ebs-snapshots-characteristics)
    - [EBS Snapshots Features](#ebs-snapshots-features)
    - [EBS Exam Tips](#ebs-exam-tips)
    - [EBS vs Instance Store](#ebs-vs-instance-store)
    - [EBS vs Instance Store Exam Tips](#ebs-vs-instance-store-exam-tips)
    - [EBS Warnings](#ebs-warnings)
- [Elastic File System](#elastic-file-system-(efs))
    - [Limits](#efs-limits)
- [Lambda](#lambda)
    - [What is Lambda?](#what-is-lambda)
    - [Why is Lambda cool?](#why-is-lambda-cool)
    - [How is Lambda priced?](#how-is-lambda-priced)
    - [Lambda Exam Tips](#lambda-exam-tips)
    - [Lambda Limits](#lambda-limits)
- [Simple Storage Service S3](#simple-storage-service-s3)
    - [S3 Features](#s3-features)
    - [S3 Versioning](#s3-versioning)
    - [S3 Lifecycle Management](#s3-lifecycle-management)
    - [Securing S3](#securing-s3)
    - [S3 Encryption](#s3-encryption)
    - [S3 Exam Tips](#exam-tips-for-s3)
- [Glacier](#glacier)
- [Storage Gateway](#storage-gateway)
    - [Storage Gateway Exam Tips](#storage-gateway-exam-tips)
- [CloudFront](#cloudfront)
    - [CloudFront Exam Tips](#cloudfront-exam-tips)
    - [Limits](#cloudfront-limits)
- [Relational Database Service (RDS)](#relational-database-service-rds)
     - [RDS Automated Backups](#rds-automated-backups)
     - [RDS Snapshots](#rds-snapshots)
     - [RDS Restore](#rds-restore)
     - [RDS Encryption](#rds-encryption)
     - [RDS Warnings](#rds-warnings)
     - [RDS Limits](#rds-limits)
     - [What is Multi-AZ RDS?](#what-is-multi-az-rds)
     - [Multi-AZ Failover](#multi-az-failover)
     - [What is Read Replica?](#what-is-read-replica)
- [DynamoDB](#dynamodb)
    - [DynamoDB Pricing](#dynamodb-pricing)
    - [DynamoDB Pricing Example](#dynamodb-pricing-example)
    - [Non-Ideal DynamoDB Scenarios](#non-ideal-dynamodb-scenarios)
    - [DynamoDB Integration](#dynamodb-integration)
    - [DynamoDB features](#dynamodb-features)
    - [Two ways to search](#two-ways-to-search)
- [ElastiCache](#elasticache)
    - [ElastiCache Exam Tips](#elasticache-exam-tips)
- [RedShift](#amazon-redshift)
    - [Architecture](#amazon-redshift-architecture)
        - [Redshift 10 times faster](#redshift-10-times-faster)
        - [Redshift Pricing](#redshift-pricing)
        - [Redshift Security](#redshift-security)
        - [Redshift Availability](#redshift-availability)
        - [Leader Node](#leader-node)
        - [Computes Nodes](#computes-nodes)
    - [Backups and Fault Tolerance](#backups-and-fault-tolerance)
- [Aurora]
    -[What is Aurora?](#what-is-aurora)
    -[Aurora Autoscaling](#aurora-autoscaling)
    -[Aurora Replicas](#aurora-replicas)
- [Understanding AWS Security](#understanding-aws-security)
    - [Physical Access](#physical-access)
    - [Security Certifications and AWS Compliance](#security-certifications-and-aws-compliance)
    - [Shared Security Responsability](#shared-security-responsability)
        - [AWS Responsibility](#aws-responsibility)
        - [Our Responsibility](#our-responsibility)
        - [Security Methods and connectivity](#security-methods-and-connectivity)
- [Route 53](#route-53)
    - [Routing Policies](#routing-policies)
    - [Route 53 Exam Tips](#route-53-exam-tips)
    - [Warnings](#route-53-warnings)
- [CloudTrail](#cloudtrail)
- [CloudWatch](#cloudwatch)
    - [What can I do with CloudWatch?](#what-can-i-do-with-cloudwatch)
    - [CloudWatch Logs](#cloudwatch-logs)
    - [Storing Logs](#storing-logs)
    - [Monitoring](#monitoring)
    - [CloudWatch Exam Tips](#cloudwatch-exam-tips)
    - [Limits](#cloudwatch-limits)
- [Trusted Advisor](#trusted-advisor)
- [Kinesis Streams](#kinesis-streams)
    - [Streams Terminology](#streams-terminology)
        - [Producers](#producers)
        - [Shards](#shards)
        - [Partition Keys](#partition-keys)
        - [Sequence Number](#sequence-number)
        - [Data Blobs](#data-blobs)
        - [Consumers](#consumers)
    - [Warnings](#kinesis-warnings)
    - [Limits](#kinesis-limits)
- [AWS CloudFormation](#aws-cloudformation)
    - [Templates and Stacks](#templates-and-stacks)
    - [Templates](#templates)
    - [Deploying Stacks](#deploying-stacks)
    - [Template Elements](#template-elements)
    - [Intrinsic Function](#intrinsic-function)
    - [Need to Know](#need-to-know)
    - [Stack Creation Errors](#stack-creation-errors)
- [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
    - [Elastic Beanstalk Overview](#elastic-beanstalk-overview)
    - [Elastic Beanstalk Management](#elastic-beanstalk-management)
    - [CloudFormation vs Elastic Beanstalk](#cloudformation-vs-elastic-beanstalk)
- [AWS OpsWorks](#aws-opsworks)
- [What is Chef?](#what-is-chef)
    - [OpsWorks Components](#opsworks-components)
- [IAM](#iam)
    - [Features](#features)
    - [Accesing IAM](#accesing-iam)   
    - [Understanding How IAM Works](#understanding-how-iam-works)
    - [Overview of Identity Management: Users](#overview-of-identity-management-users)
        - [First-Time Access Only](#first-time-access-only-your-root-user-credentials)
        - [IAM Users](#iam-users)
        - [Federating Existing Users](#federating-existing-users)
    - [Overview of Access Management: Permissions and Policies](#overview-of-access-management-permissions-and-policies)
        - [Policies and Accounts](#policies-and-accounts)
        - [Policies and Users](#policies-and-users)
        - [Policies and Groups](#policies-and-groups)
        - [Federated Users](#federated-users)
        - [Identity-based and Resource-based Policies](#identity-based-and-resource-based-policies)
    - [Security Features Outside of IAM](#security-features-outside-of-iam)
    - [IAM Best Practices and Use Cases](#iam-best-practices-and-use-cases)
    - [Identities (Users, Groups, and Roles)](#identities-users,-groups,-and-roles)
    - [Warnings](#iam-warnings)
- [Amazon SQS](#amazon-sqs)
    - [What is Amazon SQS?](#what-is-amazon-sqs)
    - [Queues Types](#queues-types)
    - [SQS Key Facts](#sqs-key-facts)
- [Amazon SWF](#amazon-swf)
    - [What is SWF?](#what-is-swf)
    - [SWF vs SQS](#swf-vs-sqs)
    - [SWF Actors](#swf-actors)
- [Amazon SNS](#amazon-sns)
    - [What is SNS?](#what-is-sns)
    - [SNS Benefits](#sns-benefits)
    - [SNS vs SQS](#sns-vs-sqs)
    - [SNS Pricing](#sns-pricing)
- [Amazon Elastic Transcoder](#amazon-elastic-transcoder)
    - [What is Elastic Transcoder](#what-is-elastic-transcoder)
- [API Gateway](#api-gateway)
    - [What is API Gateway?](#what-is-api-gateway)
    - [What is API Caching?](#what-is-api-caching)
    - [What can API Gateway do?](#what-can-api-gateway-do)
    - [Same Origin Policy](#same-origin-policy)
    - [Cross-Origin Resource Sharing (CORS)](#cross-origin-resource-sharing-cors)
    - [API Gateway Exam Tips](#api-gateway-exam-tips)
- [Kinesis](#kinesis)
    - [What is streaming data?](#what-is-streaming-data)
    - [What is Kinesis?](#what-is-kinesis) 
    - [What are the core Kinesis Services](#what-are-the-core-kinesis-services)
    - [Kinesis Exam Tips](#kinesis-exam-tips)


## VPC
* Three subnet types: Private, Public and VPN
* Single Region, multi AZs
* Security Groups:
    * Resources level traffic firewall (EC2 instance, ELB, etc..)
    * Ingress and Egress
    * Stateful
* Access Control Lists:
    * Source and Protocol filtering
    * Subnet level trafic firewall
    * Stateless
### What is a VPC?
* Think of a VPC as a virtual data center in the cloud
### VPC - AWS Definition
* You can easily customize the network configuration for your Amazon Virtual Private Cloud. For example, you can create a public-facing subnet for your webservers that has access to the Internet, and place your backend systems such as databases or application servers in a private-facing subnet with no Internet access. You can leverage multiple layers of security, including security groups and network access control lists, to help control access to Amazon EC2 instances in each subnet.
* Additionally, you can create a Hardware Virtual Private Network (VPN) connection betwwen your corporate datacenter and your VPC and leverage the AWS cloud as an extension of your corporate datacenter
### What can you do with a VPC?
* Launch instances into a subnet of your choosing
* Assign custom IP address ranges in each subnet
* Configure route tables between subnets
* Create internet gateway and attach it to our VPC
* Much better security control over your AWS resources
* Instance security groups
* Subnet network access control lists (ACLS)
### Default VPC vs Custom VPC
* Default VPS is user friendly, allowing you to inmmediately deploy instances
* All subnets in default VPC have route out to the internet
* Each EC2 instance has both a public and private IP address
### NAT Instances vs NAT Gateways
| NAT Instances                                        | NAT Gateways                                                 |                
| ---------------------------------------------------- |:------------------------------------------------------------:|     
| Use script to manage fail over between instances     | Highly available, are implement with redundancy in each AZs  |
| Depends on the bandwidth of intance type             | Is a service                                                 |
| Manage by you                                        | Managed by AWS                                               |
| A generic AMI that's configured to perform NAT       | Software is optimized for handling NAT traffic               |
| Manual port fordwarding                              | Port fordwarding NOT supported                               |
| Use a bastion server                                 | Bastion server not supported                                 |
| View CloudWatch alarms                               | Traffic metrics not supported                                |
### VPC Flow Logs
* VPC Flow Logs is a feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC. Flow log data is stored using Amazon CloudWatch Logs. After you've created a flow log, you can view and retrieve its data in Amazon CloudWatch Logs.
* Flow logs can be created a t 3 levels:
    * VPC
    * Subnet 
    * Network Interface Level

 ### VPC Peering
 * Allows you to connect one VPC with another via a direct netowork route using private Ip address
 * Instances behave as if they were on the same private network
 * You can peer VPCs's with other AWS accounts as well as with other VPCs in the same account
 * Peering is a star configuration: ie: 1 central VPC peers with 4 others. NO TRANSITIVE PEERING!
* Single region Inter-VPC routing
* Connection between same or different AWS account
* DNS supported
 ### VPC Access types
| VPN                                        | Gateways                                         |            
| ------------------------------------------ |:------------------------------------------------:| 
| Hardware-based VPN  (w/ port redundancy)   | Internet Gateway (IGW)                           |
| Direct Connect                             | Virtual Private Gateway                          |
| VPN CloudHub                               | Customer Gateway                                 |   
| Software VPN                               | Software is optimized for handling NAT traffic   |
 #### Direct Connect
* Predictable bandwidth
* Predictable performance/consistent network experience
* Support for VLAN Trunking (802.1Q)
* Can be partitioned into multiple Virtual Interfaces
#### AWS VPN CloudHub
* Direct connection to VPC for Branch offices 
### VPC Exam Tips
* Think of a VPC as a logical datacenter in AWS
* Consists of IGWs (or Virtual Privae Gateways), Route Tables, Network Access Control Lists, Subnets and Security Groups
* 1 Subnet = 1 Availability Zone
* Security Groups are Stateful; Network Access Control Lists are Stateless
* NO TRANSITIVE PEERING
* NAT Instances:
    * When creating a NAT instance, disable source/destination check on the instance
    * NAT instances must be in a public subnet 
    * There must be a route out of the private subnet to the NAT instance, in order for this to work
    * The amount of traffic that NAT instances can support depends on the instance size. If you are bottlenecking, increase the instance size
    * You can create high availability using Autoscaling Groups, multiple subnets in different AZs, and a script to automate failover
    * Behind a Security Group
* NAT Gateways:
    * Preferred by the enterprise
    * Scale automatically up to 10Gbps
    * No need to patch
    * Not associated with security groups
    * Automatically assigned a public ip address
    * Remember to update your route tables
    * No need to disable Source/Destination Checks
* Flow Logs
    * You cannot enable flow logs for VPCs that are peered with your VPC unless the peer VPC is in your account
    * You cannot tag a flow log
    * After you've created a flow log, you cannot change its configuration; for example, you can't associate a different IAM role with the flow log
    * Not all IP traffic is monitored:
        * Traffic generated by instances when they contact the Amazon DNS server. If you use your own DNS server, then all traffic to that DNS server is logged
        * Traffic generated by  Window instance for Amazon Windos licence activation
        * Traffic to and from 169.254.169.254 for instance metadata
        * DHCP traffic 
        * Traffic to the reserved IP address for the default VPC router
* NAT vs Bastions
    * A NAT is used to provide internet traffic to EC2 instances in provate subnets
    * A Bastion is used to securely administer EC2 instances (using SSH or RDP) in private subnets. They are like 'jump boxes'

### VPC Warnings
* Subnets do not span over AZs
* Update the inbound or outbound rules for your VPC Security Groups to reference Security Groups in the peered VPC
* VPC Peering: Can't overlap network addresses
* Direct Connect: 
    * Bandwidth of 1 Gbps or 10 Gbps
    * Performance and bandwidth depends on distance of AWS Region / Edge Router
### VPC Limits
* The first four IP addresses and the last IP address in each subnet CIDR block are not available for you to use, and cannot be assigned to an instance. For example, in a subnet with CIDR block 10.0.0.0/24, the following five IP addresses are reserved:
    
   * 10.0.0.0: Network address.
    
   * 10.0.0.1: Reserved by AWS for the VPC router.
    
   * 10.0.0.2: Reserved by AWS. The IP address of the DNS server is always the base of the VPC network range plus two; however, we also reserve the base of each subnet range plus two. For VPCs with multiple CIDR blocks, the IP address of the DNS server is located in the primary CIDR. For more information, see Amazon DNS Server.
    
   * 10.0.0.3: Reserved by AWS for future use.
    
   * 10.0.0.255: Network broadcast address. We do not support broadcast in a VPC, therefore we reserve this address.
* CIDR : 16-28
* VPC Peering: 50 VPC Peers per VPC, up to 125 by request

## EC2
* On-demand: paid for use
* Reserved Intances:
    * Standard
    * Scheduled
* Spot
* Dedicated:
    * Host
    * Instance
### EC2 On-demand
* Low cost and flexibility with no up front cost
* Ideal for autoscaling groups and unpredictable workloads
* Dev / Test
### EC2 Reserved Instance
* Steady state and predictable usage
* Aplications that need reserved capacity
### Spot Instances
* Flexible start and end times
* Grid computing and HPC
* Very low hourly compute cost
### Dedicated Instances
* Predictable performance
* Complete Isolation
* Most expensive
### High Performance Computing (HPC)
* Bath processing of compute intensive workloads
* Requires high performance CPU, network and storage
* Jumbo frames are typically required: Transport large amount of data quicker than over a traditional  network (a lot of I/O - NFS is suitable in this case)
    * Jumbo frame: up to 9000 bytes of data (vs standard frame only 1500 bytes)
* Supported on AWS through enhanced networking (single rout I/O virtualization (SR-IOV))
### Security Groups
* All inbound traffic is blocked by default 
* All Outbound traffic is allowed
* Changes to security gruos take effect immediately
* You can have any number of EC2 instances within a security group
* You cand have multiple security groups attached to EC2 instances
* Security groups are STATEFUL
    * If you create an inbound rule allowing traffic in, that traffic is automatically allow back out again
* You cannot block specific IP addresses using security groups, instead use Network Access Control Lists
* You can specify allo rules, but not deny rules.
### Placement Groups 
* A logical grouping of instances in a single availability zone
* Keep them as close as possible to each other in order to allow for low latency and high performance between these instances
* Can span peered VPCs (but not at full performance)

### EC2 Exam Tips
* Know the differences between:
    * On demand
    * Spot
    * Reserved
    * Dedicated hosts
* Remember with spot instances:
    * If you terminate the instance, you pay for the hour
    * If AWS terminates the spot instance, you get the hour it was terminated in for free

### Volume vs Snapshot Exam Tips
* Volumes exist on EBS:
    * Virtual Hard Disk
* Snapshots exist on S3
* Snapshots are point in time copies of Volumes
* Snapshots are incremental - this means that only the blocks that have changed since your last snapshot are moved to S3
* Snapshots of Root Device Volumes:
    * To create a snapshot for Amazon EBS volume that serve as root devices, you should stop the instance before taking the snapshot
    *  However you can take a snap while the instance is running
    * You can create AMI's from both Volumes and snapshots
    * You can change EBS volume sizes on the fly, including changing the size and storage type
    * Volumes will ALWAYS be in the same availability zone as the EC2 instance
    * To move an EC2 volume from one AZ/Region to another, take a snap or an image of it, then copy it to the new AZ/Region
* Security:
    * Snapshots of encrypted volumes are encrypted automatically
    * Volumes restored from encrypted snapshots are encrypted automatically
    * You can share snapshots, but only if they are unencrypted
        * These snapshots can be shared with other AWS accounts or made public

### EC2 Warnings
* Placement Groups: 
    * Can't span multiple availability zones
    * Reserved instances are supported on an instance level but you cannot explicity reserved CAPACITY for a placement group
    * You can't merge them 
    * The name must be unique (like S3 unique name convention) 
* The name must be unique (like S3 unique name convention) 
    * The name must be unique (like S3 unique name convention) 
    * Cannot be merged 
* Cannot be merged  
    * Cannot be merged 
    * Only certain types of intances can be launched in a placement group (Co,puted Optimized, GPU, Memory Optimized, Storage Optimized)
    * AWS recommend homogenous instances within placement groups
    * You can't move an existing instance into a placement group. You can create an AMi from your existing instance, and then launch a new instance from the AMI into a placement group
### EC2 Limits

## Load Balancer
* Instances monitored by ELB are reported as:
    * InService
    * OutofService
* Health Checks check the instance health by talking to it
* Have their own DNS name. You are never given an IP address.
* Read the ELB FAQ for Classic Load Balancers
### Classic Load Balancer (CLB)
* Region wide load balancer (not an VM / Appliance)
* Can be used internally or externally
* Layer 4 or Layer 7
* SSL termination and processing
* Cookie-based sticky sessions
* Integrate with Auto Scaling
* ELB EC2 health checks / CloudWatch
* Integrate with Route 53
* Supported ports:
    * 25 (SMTP) 
    * 80/443  (HTTP/HTTPS)
    * 1024-65535
* Support Domain Zone Apex
* Support IPv4 and IPv6
* Integrate with CloudTrail for log security analysis
* Multiple SSL certificates required multiples ELBs
* Wildcard are supported
* Associate with DNS 
### Application Load Balancer (ALB)
* Layer 7 Only
* Content-based routing
* Region Wide load balancer
* Support for microservices and containers
* Integrate with ECS
* Better performance for realtime streaming
* Reduced hourly cost
* Deletion protection
* Better health checks and CloudWatch metrics
* Listeners:
    * Define the port and protocol 
    * Each ALB needs at least on listener
    * Up to 10 listeners
    * Routing rules are defined on listeners
* Target groups:
    * Logical grouping of targets
    * Made up of EC2 instances or containers
    * Can exist independently from the ALB
    * Region-based but can be associated with an auto scaling group
* Rules:
    * Fordwards incoming request to specific target groups 
    * One or more rules
* Improved Health Check:
    * Custom response codes: 200-399
    * Detailed health check failures displayed in the API and management console
    * Detailed access to log information
    * Saved to an S3 bucket every 5 or 60 minutes
* About 10% cheaper
### LB Warnings
* Classic LB: 
    * Doesn't support Elastic IP 
    * Can't reach through IP address, only DNS name
    
## Auto Scaling     
* Elasticity
* Boostraping / Dynamic configuration
* CloudWatch or manual schedule configuration
* Notifications
* It's free
* Region Wide

## Elastic Block Storage (EBS)
* Does not need to be attached to an instance
* Can be transferred between Availability Zones
* EBS volume data is replicated across multiple servers in an Availability Zone
* Encryption of EBS data volumes, boot volumes and snapshots
* Designed for an annual failure rate (AFR) of between 0.1% - 0.2% a SLA 99.95%
### General Purpose SSD (GP2)
* General purpose, balances both price and performance
* 3 IOPS/GB (minimum 100 IOPS) to a maximum of 10,000 IOPS
* GP2 volumes smaller than 1 TB can also burst up to 3,000 IOPS
### Provisioned IOPS SSD (IO1)
* Designed for I/O intensive applications such a large relational or NoSQL databases
* Use if you need more than 10000 IOPS
* Can provision up to 20000 IOPS per volume
### Throughput Optimized HDD (ST1)
* Big data
* Data warehouses
* Log processing
* Cannot be a boot volume
### Cold HDD (SC1)
* Lowest Cost Storage for infrequently accessed workloads
* File server
* Cannot be a boot volume
### Magnetic (Standard)
* Lowest cost per gigabyte of all EBS volume types that is bootable. Magnetic volumes are ideal for workloads where data is accessed infrequently, and applications where the lowest storage cost is important
### Increasing IOPS Performance
* Multiple stripped gp2 or standard volumes (typically RAID 0)
* Multiple stripped PIOPS volumes (typically RAID 0)
* Function of the guest OS
### EBS-optimized instances
* Dedicated capacity for Amazon EBS I/O
* EBS-Optimized intances are designed for use with all EBS volume types
* Max bandwith: 400 Mbps - 12000 Mbps
* IOPS: 3000 - 65000
* gp-ssd within 10% of baseline and burst performance 99.9% of the time
* PIOPS within 10% of provisioned and burst performance 99.9% of the time
* Additional hourly fee
### EBS Snapshots Characteristics
* Point-in-time snapshot
* Supports incremental snapshots
* Billed only for changed blocks
* Deleted a snapshot removes only the data not needed by any other snapshot
### EBS Snapshots Features
* Resizing EBS volumes
* Sharing EBS snapshots 
* Coping  EBS snapshots across regions
### EBS Exam Tips
* EBS Consists of:
    * SSD, General Purpose - GP2 - (Up to 10000 IOPS)
    * SSD, Provisioned IOPS - IO1 - (More than 10000 IOPS)
    * HDD, Throughput Optimized - ST1 - frequently accessed workloads
    * HDD, Cold - SC1 - less frequently accessed data
    * HDD, Magnetic - Standard - cheap, infrequently accessed storage
### EBS vs Instance Store
* All AMIs are categorized as either backed by Amazon EBS or backed by instance store.
* For EBS Volumes: The root device for an instance launched from the AMI is an Amazon EBS volume created from an Amazon EBS snapshot
* For Instance Store Volumes: The root device for an instance launched from the AMI is an instance store volume created from a template stored in Amazon S3
### EBS vs Instance Store Exam Tips
* Instance Store Volumes are sometimes called Ephemeral Storage
* Instance Store Volumes cannot be stopped. If the underlying host fails, you will lose your data
* EBS backed instances can be stopped. You will not lose tha data on this instance if it stopped
* You can reboot both, you will no lose your data
* By default, both ROOT volumes will be deleted on termination, however with EBS volumes, you can tell AWS to keep the root device volume

### EBS Warnings
* Cannot be attached to more than one instance at the same time
* Privisioned IOPS: maximun ratio of 50:1 between IOPS and volume size

## Elastic File System (EFS)
* Simple, petabytes scalable file storage for use with EC2 instances
* EFS file systems are elastic, and automatically grow and shrink as you add and remove files
* Stored redundantly across multiples AZs
* Big Data and analytics, media processing, workflows, content management, web, home directories
* Supports NFS 4.1
* ON premises access enabled via Direct Connect
* You only pay for the storage you use (no pre-provisioning required)
* Can scale up to the petabytes
* Can support thousands of concurrent NFS connections
* Data is stored across multiple AZ's within a region
* Read After Write Consistency

### EFS Limits 
* 1 to 1000 of EC2 instances, from multiple AZs, concunrrently
* By default, you can create up to 10 file systems per AWS account per region


## Lambda
### What is Lambda?
* AWS Lambda is a compute service where you can upload your code and create a Lambda function. AWS Lambda takes care of provisioning and managing the servers that you use to run the code. You don't have to worry about operating systems, patching, scaling, etc. You can use Lambda in the following ways:
    * As an event-driven compute service where AWS Lambda runs your code in response to events. These events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table
    * As a compute service to run your code in response to HTTP requests using Amazon API Gateway or API calls made using AWS SDKs.
### Why is Lambda cool?
* No servers
* Continuous scaling
* Super cheap
### How is Lambda priced?
* Numbers of requests
    * First 1 million requests are free $0.20 per 1 million requests thereafter

* Duration
    * Duration si calculated from the time your code begins executing until it returns or otherwise terminates, rounded up to the nearest 100ms. The price depends on the amount fo memory you allocate to your function. You are charged $0.00001667 for every GB-second used
### Lambda Exam Tips
* Lambda scales out (not up) automatically
* Lambda functiosn are independent, 1 event = 1 function
* Lambda is serverless
* Know what services are serverless
* Lambda functions can trigger other lambda functions 1 event can = x functions if functions trigger other functions
* Architectures can get extremely complicated, AWS X-ray allows you to debug what is happening
* Lambda can do things globally, you can use it to back up S3 buckets to other buckets
* Know your triggers
### Lambda Limits
* Max function time: 5 minutes

## Simple Storage Service S3
### S3 Features
* File versioning
* Cross-region replication (CRR)
* Data lifecycle management 
* MFA Delete
* Permissions management
* Time-limited access to objects
### S3 Versioning
* Stores all version of an object (including all writes and even if you delete and object)
* Great backup tool 
* Once enabled, Versioning cannot be disabled, only suspended.
* Integrates with Lifecycle rules
* Versioning's MFA Delete capability, which uses multi-factor authentication, can be used to provide an additional layer of security
* Cross Region Replication, required versioning enabled on the source and destination bucket
### S3 Lifecycle Management
* Can be used in conjuntion with versioning
* Can be applied to current versions and previous versions
* Following actions can now be done:
    * Transition to the Standard - Infrequent Access Storage Class (128KB and 30 days after the creation date)
    * Archive to the Glacier Storage Class (30 days after IA, if relevant)

* 
### Securing S3
* Bucket policies
* MFA Delete
* Backing up your Bucket to another Bucket in a different account
* By default, all newly created buckets are PRIVATE
* You can setup access control to your buckets using:
    * Bucket Policies
    * Access Control Lists
* S3 buckets can be configured to create access logs which log all request made to the S3 bucket. This can be done to another bucket
### S3 Encryption
* In transit:
    * SSL/TLS
* At Rest
    * Server Side Encryption
        * S3 Managed Keys - SSE-S3
        * AWS Key Management Service, Managed Keys - SSE-KMS
        * Server side Encryption With Customer Provided Keys - SSE-C
    * Client Side Encryption

### S3 Exam Tips
* Remember that S3 is Object base i.e. allows yo to upload files.
* Files can be from 0 bytes to 5TB
* There is unlimited storage
* Files are stored in Buckets
* S3 is a universal namespace, that is, names must be unique globally
* Read after Write consistency for PUTS of new objects
* Eventual Consistency for overwrite PUTS and DELETES (can take some time to propagate)
* S3 Storage Classes/Tiers
    * S3(durable, inmediately available, frequently accessed)
    * S3 - IA(durable, immediately available, infrequently accessed)
    * S3 - Reduced Redundancy Storage (data that is easily reproducible, such as thumbnails etc)
    * Glacier - Archived data, where you can wait 3 -5 hours before accessing
* Remember the core fundamentals of S3:
    * Key (name)
    * Value (data)
    * Version ID
    * Metadata
    * Access control lists
* S3 Transfer Acceleration
    * You can spped up transfers to S3 using S3 transfer acceleration. This costs extra, and has the greatest impact on people who are in far away location.
* S3 Static Websites
    * You can use S3 to host static websites
    * Serverless
    * Very cheap, scales automatically
    * STATIC only, cannot host dynamic sites
* Write to S3 - HTTP 200 code for a successful write
* You can load files to S3 much faster by enabling multipart upload

## Glacier
* Integrates with Amazon S3 lifecycle policies
## Storage Gateway
* Gateway-cached volumes
* Gateway-stored volumes
* Gateway-virtual Tape Library (VTL)
### Storage Gateway Exam Tips
* File Gateway - For flat files, stored directly on S3
* Volume Gateway
    * Stored Volumes - Entire Dataset is stored on site and is asynchronously backed up to S3
    * Cached Volumes - Entire Dataset is stored on S3 and the most frequently accesed data is cached on site
* Gateway virtual Tape Library (VTL)
    * Used for backup and uses popular backup applications like NetBackup, Backup Exec, Veeam, etc.
## CloudFront
* A global CDN service. It integrates with other AWS products to give developers and business an easy way to distribute content to end users with low latency, high data transfer speeds and no minimum usage commitments
* Used to deliver and entire website using a global netwotk of edge locations:
    * Dynamic
    * Static
    * Streaming
    * Interactive
* Request for content is automatically routed to the nearest edge location for best possible performance
* Optimized to work with other Amazon Web Services:
    * S3
    * EC2
    * Elastic Load Balancing
    * Route 53
### CloudFront Exam Tips
* Edge Location: This is the location where content will be cached. This is separate to an AWS Region/AZ
* Origin: This is the origin of all the files that the CDN will distribute. This can be either an S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53
* Distribution: This is the name given the CDN which consists of a collection of Edge Locations
    * Web Distribution: Typically used for Websites
    * RTMP: Used for Media Streaming
* Edge locations are not just READ only, you cand write them too (Put and object on to them)
* Objects are cached for the life of the TTL (Time To Live)
* You can clear cached objects, but you will be charged

### CloudFront Limits 
* Up to 1000  vaults per region
* Individual archives can be from 1 byte to 40 terabytes

# Relational Database Service (RDS)
* Database engine manage by AWS
* MySQL, Oracle, Microsoft SQL Server, PostgreSQL, MariaDB, or Amazon Aurora
* Multi-AZ deployment options
* On-demand and reserved instance pricing
* Magnetic, gp-ssd or PIOPS
*  Oracle and Microsoft SQL licensing
    * Included Licenses
    * Bring your own license
* Automated or manual backups
## RDS Automated Backups
* There are two different types ob Backups for AWS. Automated Backups and Database Snapshots.
* Automated Backups allow you to recover your database to any point in time within a "retention period". Retention period can be between one and 35 days. Automated Backups will take a full daily snapshot and will also store transaction logs throughout the day. When you do a recovery, AWS will first choose the most recent daily back up , and then apply transaction logs relevant to that day. This allow you to do a point in time recovery down to a second, within the retention period.
* Automated Backups are enabled by default. The backup data is stored in S3 and you get free storage space equal to the size of your database. So if you have an RDS instance of 10Gb you will get 10Gb wrth of storage
* Backups are atken within a defined window. During the backup window, storage I/O may be suspended while your data is being backed up and you may experience elevated latency.
* Continuosly tracks changes and backups your database
* Volume snapshot of your entire DB instance, not just DB
* On day of backups retained by default but cand be configured up to 35 days
* Backup retention period defined during configuration
* When you delete an RDS instance, all automated snapshots are deleted. Manual snapshots are preserved
* Automated backups occurs daily during a 30 minute configurable backup window
* Automated backups are preserved for a configurable number of days (retention period)
## RDS Snapshots
* DB Snapshots are done manually (ie the are user initiated). They are stored even after you delete the original RDS instance, unlike automated backups
## RDS Restore
* RDS combines daily backups in conjuntion with transaction logs to restore the DB instance to any point during the retention period
## RDS Encryption
* Encryption at rest is supported for MySQL, Oracle, SQL Server, PostgreSQL & MariaDB. Encryption is done using the AWS Key Management Service (KMS) service. Once your RDS instance is encrypted the data stored at rest in the underlying storage is encrypted, as are its automated backups, read replicas, and snapshots.
* At the present time, encrypting an existing DB instance is not supported. To use Amazon RDS encryption for an existing database, create a new DB Instance with encryption enabled and migrate your data into it.
## RDS Warnings
* You cannot restore from a DB snapshot to an existing DB instance
* Only default DB parameters and security groups are restored
* Read Replica:
    * Used for scaling! Not for DR!
    * Must 
## RDS Limits
* Up to the last five minutes, RDS uploads transaction logs for DB instances to Amazon S3 every 5 minutes. 
## What is Multi-AZ RDS?
* Multi-AZ allows you to have an exact copy of your production database in another AvailaBility Zone. AWS handles the replication for you, so when your production database is written to, this write will automatically be synchronised to the stand by database
* In the event od planned database maintenance, DB Instance failure, or an Availability Zone failure, Amazon RDS will automatically failover to the standby so the database operations can resume quickly without administrative intervention
* Multi-AZ is for Disaster Recovery only. It is not primary used for improving performance. For performance improvement you need Read Replicas
## Multi-AZ Failover
* Multi-AZ RDS deployment designed for HA
* Synchronous replication in a secondary AZ
* DB snapshots always taken against standby instance
* AWS automatically adjusts DNS records when needed
* Multi-AZ is different from a RDS read replica
## What is Read Replica?
* Read replica's allow you to have a read only copy of your production database. THis is achived by using Asynchronous replication from the primary RDS instance to the read replica. You use read replica's primarily for very read-heavy databse workloads.
* Supported Databases: MySQL Server, PostgreSQL, MariaDB

# Amazon DynamoDB
* DynamoDB is a fully managed, highly available and scalable NoSQL database
* Automatically and synchronously replicates data across three AZ
* SSDs and limiting indexing on attributes provides high throughput and low latency
* ElasticCache can be used in front of DynamoDB
    * Offload high amounts of reads for non-frecuently changed data
* Ideal for existing or new applications that need:
    * A flexible NoSQL database with low read and write latencies
    * The ability o scale storage and throughput up or down as needed without code changes or downtime
* Amazon DynamoDB is a fast and flexible NoSQL database service for all applications that need consistentm single-digit millisecond latency at any scale. It is a fully managed database and supports both document and key-value data models. Its flexible data model and reliable performance make it a great fit for mobile, web, gaming, ad-tech, IoT and many other applications. 
* Stored on SSD storage
* Spread across 3 geographically distinct data centers
* Eventual Consistent Reads (Default)
    * Consistency across all copies of data is usually reached within a second. Repeating a read after a short time should return the updated data. (Best Read Performance)
* Strongly Consistent Reads
    * A strongly consistent read returns a result that reflects all writes that received a successful response prior to the read
## DynamoDB Pricing
* Provisioned Throughput Capacity
    * Write Throughput $0.0065 per hour for every 10 units
    * Read Throughput $0.0065 per hour for every 50 units
* Storage costs of $0.25 per GB of data per month
## DynamoDB Pricing Example
* Let's assume that your application needs to perform 1 million writes and 1 million reads per day, while storing 3 GB of data. First, you need to calculate how many writes and reads per second you need. 1 million evenly spread writes per day is equivalent to 1.000.000 (writes) / 24 (hours) / 60 (minutes) / 60 (seconds) = 11.6 writes per second.
* A DynamoDB Write Capacity Unit can handle 1 write per second, so you need 12 Write Capacity Units. Similary, to handle 1 million strongly consistent reads per day, you need 12 Read Capacity Units. With Read Capacity Units, you are billed in blocks of 50, with Write Capacity Units you are billed in blocks of 10.
* To calculate Write Capacity Units = (0.0065/10) x 12 x 24 = $0.1872
* To calculate Rrite Capacity Units = (0.0065/50) x 12 x 24 = $0.0374

## Non-Ideal DynamoDB Scenarios
* Pre-written applications tied to a traditional relational database
* Join and/or complex transactions
* BLOB data (binary large objects)
* Large data with low I/O rate
## DynamoDB Integration
* Amazon Elastic MapReduce: Allows enterprises perform analytics of large datasets
* Amazon RedShift: enable advanced bussiness intelligence
* Amazon Data Pipeline: Automates data movement in/out  DynamoDB
* Amazon S3: workloads that requires BLOB
* Management console and Apis
## DynamoDB features
* Stores structured data in tables, indexes by a primary key
* Tables are collection of items and items are made up of attributes (columns)
* Primary Key can be:
    * Single-attribute hash key
    * Composite hash-range key
* Secondary Index: increases performance, offload some of the workload
* Streams: Allow you to keep track of item level changes or to get a list of all item level changes that have occur in the last 24 hrs
* Cross-region replication: with low latency access
* Triggers: Event driven triggers
* Schemaless: Flexible database
## Two ways to search
* Query operation: find items in a table or secondary index using only primary key attribute
* Scan operation : find every item in a table or in a secondary index. By default it will return all data attributes for every item in a table or a index. Heavy, overhead, pull down performance

# ElastiCache
* ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory cache in the cloud. The service improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slower disk-based databases 
* Amazon ElastiCache can be used to significantly improve latency and throughput for many read-heavy application workloads (such as social networking, gaming media sharing and Q&A portals) or computing intensive workloads (such as a recommendation engine)
* Caching improves application performance by storing critical pieces of data in memory for low-latency access. Cached information may include the results of I/O-intensive database queries or the results of computationally-intensive calculations.
* Open-source in-memory caching engines
    * Memcached:
        * A widely adopted memory object caching system. ElastiCache is protocol compliant with Memcached, so popular tools that you use today with existing Memcached environments will work seamlessly with the service.
    * Redis:
        * A Popular open-source in-memory key-value store that supports data structures such as sorted sets and lists. ElastiCache supports Master/Slave replication and Multi-AZ which can be used to achieve cross AZ redundancy
* Master/Slave replication and Multi-AZ
    * Can be used to achieve cross AZ redundancy

| Feature                   | Memcached  | Redis  |                
| --------------------------|:----------:|:------:|     
| Cache to offload DB       | ✓          |✓       |
| Multithreaded performance | ✓          |✕       |
| Horizontal scanning       | ✓          |✕       |
| Multi AZ                  | ✕          |✓       |
| Backup and restore        | ✕          |✓       |
| Pub/Sub functionality     | ✕          |✓       |
| Sorting and ranking       | ✕          |✓       |
| Advanced data types       | ✕          |✓       |
| Persistence               | ✕          |✓       |
## ElastiCache Exam Tips
* Typically you will be given a scenario where a particular database is under a lot of stress/load. You may be asked which service you should use to alleviate this.
* Elasticache is a good choice if your database is particularly read heavy and not prone to frequent changing
* Redshift is a good answer if the reason your database is feeling stress is because management keep running OLAP transactions on it.

# Amazon RedShift 
* Fast and fully managed petabyte-scale relational data warehouse service.
* Analyze all your data using your existing bussines intelligence tools.
* HDD and SSD platforms.
* Starts at $0.25/hour
* Scale to $1000/TB/year
* Amazon Redshift is a fast and powerful, fully managed, petabyte-scale data warehouse service in the cloud. Customers can start small for just $0.25 per hour with no commitments or upfront costs and scale to a petabyte or more for $1,000 per terabyte per year, less than a tenth of most other data warehousing solutions
## Amazon RedShift Architecture
* Single Node (160GB)
* Multi-Node
    * Leader Node (manages client connections and receives queries)
    * Compute Node (store data and perform queries and computations). Up to 128 Compute Nodes
## Redshift 10 times faster
* Columnar Data Storage: Instead of storing data as series of rows, Amazon Redshift organizes the data by column. Unlike row-based systems, which are ideal for transaction processing, column-based system are ideal for data warehousing and analytics, where queries often involve aggregates performed over large data sets. Since only the columns involved in the queries are processed and columnar data is stored sequentially on the storage media, column-based systems require far fewer I/Os, greatly improving query performance
* Advanced Compression: Columnar data stores can be compressed much more than row-based data stores because similar data is stored sequentially on disk. Amazon Redshift employs multiple compression relative to traditional relational data stores. In addition, Amazon Redshift dosen't require indexes or materialized views and so uses less space than traditional relational databases systems. When loading data into an empty table, Amazon Redshift automatically samples your data and selects the most appropiate compresion scheme
 * Massively Parallel Processing (MPP): Amazon Redshift automatically distributes data and query load across all nodes. Amazon Redshift makes it easy to add nodes to your data warehouse and enables you to maintain fast query performance as your data warehouse grows.
 ## Redshift Pricing
 * Compute Node Hours (total number of hours you run across all your compute nodes for the billing period. You are billed for 1 unit per node per hourm, so a 3-node data warehouse cluster running persistently for an entire month would incur 2,160 instance hours. You will not be chrged for leader node hours; only compute nodes will incur charges)
 * Backup
 * Data transfer (only within a VPC, not outside it)
 ## Redshift Security
 * Encrypted in transit using SSL
 * Encrypted at rest using AES-256 encryption
 * By default Redshift takes care of key management
    * Manage your own keys through HSM
## Redshift Availability
* Currently only available in one AZ
* Can restore snapshots to new AZ's in the event of an outage

### Leader Node
* Simple SQL end point
* Stores metadata
* Optimizes query plan
* Coordinates query execution
### Computes Nodes
* Local columnar storage 
* Parallel/distributed execution of all queries, loads, backups , restores, resizes
## Backups and Fault Tolerance
* Continuous/Incremental backups
    * Multiple copies within cluster 
    * Continuous and incremental backups to S3
    * Continuous and incremental backups across regions
    * Streaming restore
* Fault Tolerance
    * Disk failures
    * Node failures
    * Network failures
    * Availability zone/region level disasters
* Security 
    * Load encrypted from S3
    * SSL to secure data in transit 
    * Amazon VPc for network isolation
    * Encryption to secure data at rest
    * Audit logging and AWS CloudTrail integration
    * SOC 1/2/3, PCI-DSS, FedRamp, BAA
# Aurora
## What is Aurora?
* Amazon Aurora is a MySQL-compatible, relational database engine that combines the speed and availability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases. Amazon Aurora provides up to five times better performance that MySQL at a proce point one tenth that of a commercial database while delivering similar performance and availability
## Aurora Scaling
* Start with 10GB, scales in 10GB increments to 64GB (Storage Autoscaling)
* Compute resources can scale up to 32vCPUs and 244GB of memory
* 2 copies of your data is containe in each availability zone, with minimun of 3 availability zones. 6 copies of your data
* Aurora is designed to transparently handle the loss of up to two copies of data without affecting database write availability and up to three copies without affecting read availability
* Aurora storage is also self-healing. Data block and disks are continuously scanned for errors and repaired automatically
## Aurora Replicas
* 2 types of Replicas are available
* Aurora Replicas (up to 15)
* MySQL Read Replicas (up to 5)

# Understanding AWS Security
## Physical Access
* Secrets locations
* Controlled physical access
* Best in class datacenter security
* Video Surveillance
* Hardware refresh cycle to avoid component failure 
* Properly decommisioned storage
* Always on Monitoring System
## Security Certifications and AWS Compliance
|                           |                  
| --------------------------|    
| HIPAA       
| SOC 1/SSAE 16/ISAE 3402 
| SOC2       
| SOC 3                  
| PCI DSS Level 1        
| ISO 27001     
| FedRAMP(SM)       
| DIACAP and FISMA      
| ITAR              
| FIPS 140-2              
| CSA          
| MPAA              

## Shared Security Responsability
### AWS Responsibility
* Virtual host security
* Storage security 
* Network security
* Data center security
* Database Security
### Our Responsibility
* AWS account security (MFA, API)
* Operating system
* Database
* Applications
* Data Encryption
* Authentication
* Network integrity
### Security Methods and connectivity
* Virtual Private Cloud (VPC)
* Dedicated connectivity
* Encryption
* Web Application Firewalls (WAF)
* DDoS Mitigation
* Dedicated Servers
* Inventory and Configuration
* Monitoring and Logging
* Penetration Testing

## Route 53
* Named after TCP 53 / UDP 53 ports
* World wide distributed DNS
* Database of name to ip mappings
* Route 53 has a 100% SLA (Service-level agreement)
* Route 53 API
* Server Health check
* Public Hosted Zone
* Public Hosted Zone for Amazon VPC (naem resolution for EC2 instances)
* You can extend on-premises DNS to Amazon VPC

| Type  |           Description       | Function  |                
| ------|:---------------------------:|:------|     
| A     | Address Record              | Returns a 32-bit IPv4 address, most commonly used to map hostnames to an IP address of the host, but it is also used for DNSBLs, storing subnet masks in RFC 1101, etc. 
| CNAME | Canonical Name record | Alias of one name to another: the DNS lookup will continue by retrying the lookup with the new name.
| MX    | Mail exchange record | Maps a domain name to a list of message transfer agents for that domain
| AAAA  | IPv6 address record | Returns a 128-bit IPv6 address, most commonly used to map hostnames to an IP address of the host.
| PTR   | Pointer record | Pointer to a canonical name. Unlike a CNAME, DNS processing stops and just the name is returned. The most common use is for implementing reverse DNS lookups, but other uses include such things as DNS-SD. 
| SRV   | Service locator | Generalized service location record, used for newer protocols instead of creating protocol-specific records such as MX.
| SPF   |  | 
| NS    | Name server record | Delegates a DNS zone to use the given authoritative name servers
| SOA   | Start of [a zone of] authority record | Specifies authoritative information about a DNS zone, including the primary name server, the email of the domain administrator, the domain serial number, and several timers relating to refreshing the zone.
### Routing Policies
* Single (simple)
    * You can associate an A record with one or more IP addresses
    * Single simply does round robin routing policies among several IP addresses
    * Single does not support any health checks
* Weighted
    * Very similar to single but you can specify a weight per IP address 
    * Weight represents a numerical value that favors one IP address over another
* Latency
    * AWS will maintain a database of latencies from different parts of the world
    * Based on the table that AWS maintains, the user is routed to the lowest latency server
* Failover
    * Failover allows you to failover to a secondary IP address
    * Failover is associated with health checks
* Geolocation
    * Caters to differents users in different countries and different languages
    * Contains users within a particular geography and offers them a customized version of the workload that caters to their specific needs
### Route 53 Exam Tips 
* ELB's do not have pre-defined IPv4 addresses, you resolve to them using a DNS name
* Understand the difference between an Alias Record and a CNAME:    
    Differences between the A, CNAME, ALIAS and URL records
    A, CNAME, ALIAS and URL records are all possible solutions to point a host name (name hereafter) to your site. However, they have some small differences that affect how the client will reach your site.

    Before going further into the details, it’s important to know that A and CNAME records are standard DNS records, whilst ALIAS and URL records are custom DNS records provided by DNSimple’s DNS hosting. Both of them are translated internally into A records to ensure compatibility with the DNS protocol.

    Understanding the differences
    Here’s the main differences:

    The A record maps a name to one or more IP addresses, when the IP are known and stable.
    The CNAME record maps a name to another name. It should only be used when there are no other records on that name.
    The ALIAS record maps a name to another name, but in turns it can coexist with other records on that name.
    The URL record redirects the name to the target name using the HTTP 301 status code.
    Some important rules to keep in mind:

    The A, CNAME, ALIAS records causes a name to resolve to an IP. Vice-versa, the URL record redirects the name to a destination. The URL record is simple and effective way to apply a redirect for a name to another name, for example to redirect www.example.com to example.com.
    The A name must resolve to an IP, the CNAME and ALIAS record must point to a name.
    Which one to use
    Understanding the difference between the A name and the CNAME records will help you to decide.

    The general rule is:

    use an A record if you manage what IP addresses are assigned to a particular machine or if the IP are fixed (this is the most common case)
    use a CNAME record if you want to alias a name to another name, and you don’t need other records (such as MX records for emails) for the same name
    use an ALIAS record if you are trying to alias the root domain (apex zone) or if you need other records for the same name
    use the URL record if you want the name to redirect (change address) instead of resolving to a destination.
    You should never use a CNAME record for your root domain name (i.e. example.com).
* Given the choice, always choose an Alias Record over a CNAME
* Remember the different routing policies and their use cases
    * Simple
    * Weighted
    * Latency
    * Failover
    * Geolocation
### Route 53 Warnings
* You cannot extend Route 53 to on-premises instances
* Cannot automatically register EC2 instances with private hosted zones

## CloudTrail
* A web service that records AWS API calls for your account and delivers log files to you
* Recorded information includes 
    * The identity of the API caller
    * The time of the API call
    * The source IP address of the API caller
    * The request parameters
    * The response elements returned by the AWS service
* Is not enabled by default
* Can be extended on a per region basis
* Save a history of  API calls for your AWS account
* API history enables security analysis, resource change tracking, and compliance auditing
* Logs API call made via:
    * AWS Management Console
    * AWS SDKs
    * Command Line Tools
    * High-level AWS Services (Such as AWS CloudFormation)
## CloudWatch
* Collects and track metrics
* Collect and monitor log files
* Set alarms
* Automatically react to changes in your AWS resources
* Monitor AWS resources such as:
    * Amazon EC2 instances
    * amazon DynamoDB tables
    * Amazon RDS DB instances
    * Custom metrics generated by your applications and services
    * Any log files your applications generate
* Gain system-wide visibility into resource utilization
* Application performance
* Operational Health
### What can I do with CloudWatch?
* Dashboards - Creates awesome dashboards to see what is happening with your AWS environment
* Alarms - allows you to set Alarms that notufy you when particular thresholds are hit
* Events - CloudWatch Events helps you to respond to state changes in your AWS resources
* Logs - CloudWAtch logs helps you to aggregate, monitor and store logs 

### CloudWatch Logs
* By default, CloudWatch logs will store your log data indefinitely
* CloudTrail logs can be sent to CloudWatch logs for real-time monitoring
* CloudWatch log metric filters can evaluate CloudTrail logs for specific terms, phases, or values 
* You can assing CloudWatch metrics to the metric filters
* You can create CloudWatch alarms
### Storing Logs
* CloudWach Logs
* Centralized logging system (Splunk)
* Custom script and store on S3
### Monitoring
* Do not store logs on non-persistent disks
    * EC2 instances root volume
    * Ephemeral storage
* Best practice is to store logs in CloudWatch logs or S3
* CloudTrail can be used across multiple AWS accounts while being pointed to a single S3 bucket (requires cross account access)
* CloudWatch logs subscription can be used across multiple AWS accounts (requires cross account access)
### CloudWatch Exam Tips
* Standard Monitoring = 5 minutes
* Detailed Monitoring = 1 minute
### CloudWatch Limits
* Alarm history is stored for 14 days 

## Trusted Advisor
* A service that helps you reduce cost, increase performance, and improve security by optimizing your AWS environment.
* Provides real time guidance to help you provision resources following AWS best practices
* Automated AWS account audits
    * Cost 
    * Performance
    * Security
    * Fault Tolerance
    * Paid version expands number of areas audited

## Kinesis Streams
* Enables you to build custom applications that process or analyze streaming data for specialized needs.
* It can continuously capture and store TB of data per hour from thounsand of sources such as websites, clickstreams, fincial transactions, social media feeds, IT logs and location-tracking events
### Streams Terminology
#### Producers
* EC2 instances
* Client
* Mobile Clients
* Traditional Servers
* Can initiate stream to:
    * Amazon Kinesis
    * Streams API
    * Amazon Kinesis Produce Library (KPL, store for example on GitHub)
    * Amazon Kinesis Agent (install on Mobile Client)
#### Shards
* A uniquely identified group of data records in a stream
* A stream is composed of one or more shards, each of which provides a fixed unit capacity
#### Partition Keys
* Used to group data by shard within a stream
* Stream service segregates data records belonging to a stream into multiple shards
* Use partition keys associated with each data record to determine which shard a given data record belong to
* Specified by the applications putting the data into a stream
#### Sequence Number
* Each data record has a unique sequence number
* Assinged by streams after you write to the stream with client.putRecords or client.putRecord
#### Data Blobs
* The data your producer adds to a stream. The maximun size of data blob (the data payload after base64-decoding) is 1 Megabyte (MB)
#### Consumers
* Consumers get records from Amazon Kinesis Streams and process then these consumers are known as Amazon Streams Applications 
### Kinesis Warnings
* By default data is stored for 24 hours, but can be increased up to 7 days
### Kinesis Limits
* Can support up to 5 transactions per second for reads
* Max total data read rate of 2 MB/s
* Up to 1000 records per seconds of writes
* Max total data write rate of 1 MB/s (including partition keys)

## AWS CloudFormation
* Gives developers and system administrators an easy way to create and manage a collection fo related AWS resources provisioning and updating them so in an orderly and predictable fashion
### Templates and Stacks
| Templates|Stacks|                
| ------|---------------------------
| Templates are architectural designs     | Stacks are deployed resources 
| You can create, update and delete templates | You can create, update and delete stacks using templates
| CloudFormation templates are written in JSON 
### Templates
* You don't need to figure out the order for provisioning AWS services
* You don't need to worry about making dependencies to work 
* Modify and update templates ina a controlled and predictable way
    * In effect applying version control
* Visualize with the AWS Cloudformation Designer
### Deploying Stacks
* AWS Management Console
* Command Line Interface
* APIs
### Template Elements
* File format and version (required)
* List of resources and associated configuration values (required)
* Template parameters (optional - up to 60)
* Output values(optional - up to 60)
* List of data tables
### Intrinsic Function
* Provides several built-in functions that help you manage your stacks 
* Assing values to properties that are not available until runtime
* Functions include: Fn::Base64, condition functions, Fn::FindInMap, Fn::GetAZs, Fn::Join, Fn::Select
### Need to Know
* Puppet and Chef integration
* Bootstrap scripts
* Define deletion policies
* Provides wait condition
* Create roles in IAM
* VPCs can be created and customized
* VPC peering in the same AWS account
* Route 53 supported
### Stack Creation Errors
* Automatic rollback on error is enabled by default 
* You will be chrged for resources provisioned even if there is an error
* CloudFormation is free

## AWS Elastic Beanstalk
* A service for deploying and scaling web applications and services
* Upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring
### Elastic Beanstalk Overview
* Integrates with VPC
* Integrates with IAM
* Can provision RDS instances
* Full control of resources
* Code is stored in S3
* Multiple environment are supported to enable versioning
* changes from git repositories are replicated
* Linux and Windows 2008 R2 AMI support
* Deploy code using a WAR file or git repository
* Use AWS toolkit for Visual Studio and AWS toolkit for Eclipse to deploy to Elastic Beanstalk
* Elastic Beanstalk is fault tolerant within a single region (not fault tolerant between regions)
* By default your applications are publicy accesible
### Elastic Beanstalk Management
* CloudWatch monitoring
* Adjust application server settings
* Run other application components
* Access log files without logging into application servers
### CloudFormation vs Elastic Beanstalk
* cloudformation supports Elastic Beanstalk
* Elastic Beanstalk does not provisions CloudFormation templates
* Elastic Beanstalk is ideal for developers with limited cloud experience that nedd to deploy environments fast
* Elastic Beanstalk is ideal if you have a standard PHP, Java, Python, Ruby, Node.js, .NET, Go, or Docker application that can run on an App server with database

## AWS OpsWorks 
* A configuration management service that helps you automate operational tasks like software configuration, package installations, database setups, server scaling, and code deployment using chef
### What is Chef?
* Automation platform that transform infraestructure into code
* automates how applications are configured, deployed, and managed across your network
* Chef server stores your recipes and configuration data
* chef client (node) is installed on each server
### OpsWorks Components
* Use the AWS Management Console
* Consists of two elements: Stack and Layers
* Stacks are containers of resources (EC2, RDS, ELB) that you want to manage collectively
* Every stack contains one or more layers:
    * Web application layer
    * Database layer
* Layers automate the deployment of packages for you

## IAM
* AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.
### Features
* Shared access to your AWS account
* Granular permissions
* Secure access to AWS resources for applications that run on Amazon EC2
* Multi-factor authentication (MFA)
* Identity federation 
* PCI DSS Compliance
* Integrated with many AWS services
* Eventually Consistent
* Free to use
### Accesing IAM
* AWS Management Console
* AWS Command Line Tools
* AWS SDKs
* IAM HTTPS API

### Understanding How IAM Works
The IAM infrastructure includes the following elements:
* **Principal**: Make a request for an action or operation on an AWS resource. Users, roles, federated users, and applications are all AWS principals.
* **Request**: The principal sends a request to AWS when  tries to use the AWS Management Console, the AWS API, or the AWS CLI, 
* **Authentication**: As a principal, you must be authenticated (signed in to AWS) to send a request to AWS.
* **Authorization**: During authorization, AWS uses values from the request context to check for policies that apply to the request. It then uses the policies to determine whether to allow or deny the request.
* **Actions or Operations**: Things that you can do to a resource, such as viewing, creating, editing, and deleting that resource. 
* **Resources**: A resource is an object that exists within a service. 
### Overview of Identity Management: Users
#### First-Time Access Only: Your Root User Credentials
When you create an AWS account (with password and email), you create an AWS account root user identity. This combination of your email address and password is also called your **root user credentials**.
#### IAM Users
You can create individual IAM users within your account that correspond to users in your organization. IAM users are not separate accounts.
#### Federating Existing Users
If the users in your organization already have a way to be authenticated, such as by signing in to your corporate network, you don't have to create separate IAM users for them. Instead, you can federate those user identities into AWS.
Federation is particularly useful in these cases:
* Your users already have identities in a corporate directory.
* Your users already have Internet identities.
### Overview of Access Management: Permissions and Policies
Access management define what a user or other entity is allowed to do in an account. This process is often referred to as authorization.
#### Policies and Accounts
If you manage a single account in AWS, then you define the permissions within that account using policies.
#### Policies and Users
ou give permissions to a user by creating an identity-based policy, which is a policy that is attached to the user
#### Policies and Groups
You can organize IAM users into IAM groups and attach a policy to a group. 
#### Federated Users 
Federated users don't have permanent identities in your AWS account the way that IAM users do. To assign permissions to federated users, you can create an entity referred to as a role and define permissions for the role. 
#### Identity-based and Resource-based Policies
 *Identity-based policies*  are permissions policies that you attach to a principal (or identity), such as an IAM user, group, or role. 
* **Managed policies** – Standalone identity-based policies that you can attach to multiple users, groups, and roles in your AWS account. Two types:
     * AWS managed policies – Managed policies that are created and managed by AWS. 
     * Customer managed policies – Managed policies that you create and manage in your AWS account.
 * **Inline policies** – Policies that you create and manage and that are embedded directly into a single user, group, or role.
 *Resource-based policies* control what actions a specified principal can perform on that resource and under what conditions. Resource-based policies are inline policies, and there are no managed resource-based policies.
 *Trust policies* are resource-based policies that are attached to a role.  They define which principals can assume the role.
### Security Features Outside of IAM
Some AWS products have other ways to secure their resources
* Amazon EC2: You log into an instance with a key pair (for Linux instances) or using a user name and password (for Microsoft Windows instances).
* Amazon RDS: You log into the database engine with a user name and password that are tied to that database.
* Amazon EC2 and Amazon RDS: You use security groups to control traffic to an instance or database.
* Amazon WorkSpaces: Users sign in to a desktop with a user name and password.
* Amazon WorkDocs: Users get access to shared documents by signing in with a user name and password.
### IAM Best Practices and Use Cases
 * Lock Away Your AWS Account Root User Access Keys
 * Create Individual IAM Users
 * Use Groups to Assign Permissions to IAM Users
 * Use AWS Defined Policies to Assign Permissions Whenever Possible
 * Grant Least Privilege
 * Use Access Levels to Review IAM Permissions
 * Configure a Strong Password Policy for Your Users
 * Enable MFA for Privileged Users
 * Use Roles for Applications That Run on Amazon EC2 Instances
 * Use Roles to Delegate Permissions
 * Do Not Share Access Keys
 * Rotate Credentials Regularly
 * Remove Unnecessary Credentials
 * Use Policy Conditions for Extra Security: restrict IP address, enable MFA
 * Monitor Activity in Your AWS Account
 ### Identities (Users, Groups, and Roles)
* The AWS Account Root User
* IAM Users
* IAM Groups
* IAM Roles 
* Temporary Credentials
### IAM Warnings
* If a request to change some data is successful, the change is committed and safely stored. However, the change must be replicated across IAM, which can take some time. Such changes include creating or updating users, groups, roles, or policies. We recommend that you do not include such IAM changes in the critical, high-availability code paths of your application. 
* Policies and Users: Actions or resources that are not explicitly allowed are denied by default.
* You cannot attach a resource-based policy to an IAM identity.

# Amazon SQS
## What is Amazon SQS?
* Amazon SQS is a web service that gives you access to a message queue that can be used to store messages while waiting for a computer to process them. 
* Amazon SQS is a distributed queue system that enables web service applications to quickly and reliably queue messages that one component in the application generates to be consumed by another component. A queue is a temporary repository for messages that are awaiting processing
* Using Amazon SQS, you can decouple the components of an application so they run independently, with Amazon SQS easing message management between components. Any component of a distributed application can store messages in a fail-safe queue. Messages can contain up to 256 KB of text in any format. Any component can later retrieve the messages programmatically using the Amazon SQS API
* The queue acts as a buffer between the component producing and saving data, and the component receiving the data for processing. This means the queue resolves issues that arise if the producer is producing work faster than the consumer can process it, or if the producer or consumer are only intermittently connected to the network
## Queues Types
* Standard Queues (default)
    * Amazon SQS offers standard as the default queue type. A standard queue lets you have a nearly-unlimited number of transactions per second. Standard queues guarantee that a message is delivered at least once.
    However, occasionally (due of the highly-distributed architecture that allows high throughput), more that one copy of a message might be delivered out of order. Standard queues provide best-effort ordering which ensures that messages are generally delivered in the same order as they are sent
* FIFO Queue 
    * The FIFO queue complements the standard queue. The most important features of this queue type are FIFO (first-in-first-out) delivery and exactly-once processing: The order in which messages are sent and received is strictly preserved and a message is delivered once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue. FIFO queue also support message groups that allow multiple ordered message groups within a single queue. FIFO queues are limited to 300 transactions per second (TPS), but have all the capabilities of standard queues
## SQS Key Facts
* SQS is pull based. noy pushed base
* Messages are 256 KB in size
* Messages can be kept in the queue from 1 minute to 14 days. The default is 4 days
* Visibility Time Out is the amount of time that the message is invisible in the SQS queue after a reader picks up that message. Provided the job is processed before the visibility time out expires, the message will then be deleted from the queue. If the job is not processed within that time, the message will become visible again an another reader will process it. This could result in the same message being delivered twice
* Visibility Time Out is 12 hours
* SQS guarantees that your messages will be processed at least once.
* Amazon SQS long polling is a way to retrieve messages from your Amazon SQS queues. While the regular short polling returns inmediately, even if the message queue being polled is empty, long polling dosen't return a response until a message arrives in the message queue, or the pong poll times out
# Amazon SWF
## What is SWF?
* Amazon Simple Workflow Service (Amazon SWF) is a web service that makes it easy to coordinate work across distributed application components. Amazon SWF enables applications for range of use cases, including media processing, web application back-ends, bussines process workflows, and analytics pipelines, to be designed as a coordination of tasks. Tasks represent invocations of variuos processing steps in an application which can be performed by executable code, web service calls, human actions , and scripts

## SWF vs SQS
* SQS has a retention period of 14 days, SWF up to 1 year for workflow executions
* Amazon SWF presents a task-oriented API, whereas Amazon SQS offers a message-oriented API
* Amazon SWF ensures that a task is assigned only once and is never duplicated. With Amazon SQS, you need to handle duplicated messages and may also need to ensure that a message is processed only once
* Amazon SWF keeps track of all the tasks and events in an application. With Amazon SQS, you need to implement your own application-level tracking, especially if your application uses multiples queues
## SWF Actors
* Workflow Starters: An application that can initiate (start) a workflow. Could be your e-commerce website when placing an order or a mobile app searching for bus times
* Deciders: Control the flow of activity tasks in a workflow execution. If something has finished in a workflow (or fails) a Decider decides what to do next
* Activity Workers: Carry out the activity tasks
# Amazon SNS
## What is SNS?
* Amazon Simple Notification Service (Amazon SNS) is a web service that makes it easy to set up, operate, and send notifications from the cloud. It provides developers with a highly scalable, flexible, and cost-effective capability to publish messages from an application and inmediately deliver them to subscribers or other applications
* Push notifications to Apple, Google, Fire OS and Windows devices, as well as Android devices in China with Baidu Cloud Push
* Besides pushing cloud notifications directly to mobile devices, Amazon SNS can also deliver notifications by SMS text message or email, to Amazon Simple Queue Service (SQS) queues, or to any HTTP endpoint. SNS notifications can also trigger Lambda functions. When a message is published to an SNS topic that has a Lambda function subscribed to it, the Lambda function is invoked ith the payload of the published message. The Lambda function receives the message payload as an input parameter and can manipulate the information in the message, publish the message to other SNS topics, or send the message to other AWS services
* SNS alows you to gropu multiple recipients using topics. A topic is an "access point" for allowing recipients to dynamically subscribe for identical copies of the same notification. One topic can support deliveries to multiple endpoint types -- for example, you can group together iOS, Android and SMS recipients. When you publish once to a topic, SNS delivers appropiately formatted copies of your message to each subscriber
## SNS Benefits
* Instantaneous, push-based delivery (no polling)
* Simple APIs and easy integration with applications
* Flexible message delivery over multiple transport protocols
* inexpensive, pay-as-you-go model with no up-front costs
* Web-based AWS Management Console offers the simplicity of a point-and-click interface
## SNS vs SQS
* Both Messaging Services in AWS
* SNS: Push
* SQS: Polls (Pulls)
## SNS Pricing
* Users pay $0.50 per 1 million Amazon SNS requests
* $0.06 per 100.000 Notifications deliveries over HTTP
* $0.75 per 100 Notifications deliveries over SMS
* $2.00 per 100.000 Notification deliveries over Email

# Amazon Elastic Transcoder
## What is Elastic Transcoder?
* Media Transcoder in the Cloud. 
* Convert media files from their original source format in to different formats that will play on smartphones, tables, PC's etc.
* Provides transcoding presets for popular output formats, which means that you don't need to guess about which settings work best on particular devices.
* Pay based on the minutes that you transcode and the resolution at which you transcode

# API Gateway
## What is API Gateway?
* Amazon aPI Gateway is a fully managed service that makes it eas for developers to publish, maintain, monitor, and secure APIs at any scale. With a few clicks in the AWS Management Console, you can create an API that acts as a "front door" for applications to access data, bussines logic, or functionality from your back-end services, such as applications running on Amazon Elastic Compute Cloud (Amazon EC2), code running on AWS Lambda, or any web application
## What is API Caching? 
* You can enable API caching in Amazon API Gateway to cache your endpoint's response. With caching, you can reduce the number of calls made to your endpoint and also improve the latency of the requests to your API. When you enable caching for stage, API Gateway caches responses from your endpoint for a specified time-to-live (TTL) period, in seconds. API Gateway then responds to the request by looking up the endpoint response from the cache instead of making a request to your endpoint
## What can API Gateway do?
* Low cost & efficient
* Scales effortlessly
* You can throttle requests to prevent attacks
* Connect to CloudWatch to log all requests

## Same Origin Policy 
* In computing, the same-origin policy is an important concept in the web application security model. Under the policy, a web browser permits scripts contained in a first web page to access data in a second web page, but only if both web pages have the same origin
## Cross-Origin Resource Sharing (CORS)
* CORS is one way the server ar the other end (not the client code in the browser) can relax the same-origin policy
* Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources (e.g. fonts) on a web page to be requested from another domain outside the domain from which the first resource was served.
* Error - "Origin policy cannot be read at the remote resource?". You need to enable CORS on API Gateway
## API Gateway Exam Tips
* Remember what API Gateway is at a high level
* API Gateway has caching capabilities to increase performance
* API Gateway is low cost and scales automatically 
* You can throttle API Gateway to prevent attacks
* You can log results to CloudWatch
* If you are using Javascript/AJAX that uses multiple domains with API Gateway, ensure that you have enabled CORS on API Gateway

# Kinesis
## What is streaming data?
* Streaming data is data that is generated continuosly by thounsands of data sources, which typically send in the data records simultaneously, and in small sizes (order of Kilobytes).
    * Purchases from online stores (think amazon.com)
    * Stock prices
    * Game data (as the gamer plays)
    * Social network data
    * Geospatial data (think uber.com)
    * IoT sensor data
## What is Kinesis?
* Amazon Kinesis is a platform on AWS to send your streaming data too. Kinesis makes it easy to load and analize streaming data, and also providing the ability for you to bould your own custom applications for you bussines needs
## What are the core Kinesis Services
* Kinesis Streams:
    * Kinesis Streams consist of shards
        * Store data in shards
        * 5 transactions per second for reads, up to a maximum total data read rate of 2 MB per second and up to 1.000 records per second for writes, up to a maximun total data write fo 1 MB per second (including partition keys)
        * The data capacity of your stream is a function of the number of shards that you specify for the stream. The total capacity of the stream is the sum of the capacities of its shards
* Kinesis Firehose:
    * Used to capture and send data directly into S3 or RedShift
    * Once data is stores in S3 or RedShift, it can be used for analisys
    * Needs agent in between to capture data nito the stream. i.e. Kinesis Agent
    * Has an option to buffer the data from the incoming stream. So that there will be no loss of data
* Kinesis Analitycs
    * A way to analize data from Kinesis using SQL queries

 ## Kinesis Exam Tips
 * Know the difference between Kinesis Streams and Kinesis Firehose. You will be given scenario questions and you must choose the most relevant choice
 * Understand what Kinesis Analitycs is

