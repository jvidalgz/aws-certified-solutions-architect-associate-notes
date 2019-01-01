AWS Certified Solutions Architect  Associate -  Notes
=====================================
- [VPC](#vpc)
    - [NAT Instances vs NAT Gateways](#nat-instances-vs-nat-gateways)
    - [VPC Peering](#vpc-peering)
    - [VPC Access types](#vpc-access-types)
        - [Direct Connect](#direct-connect)
        - [AWS VPN CloudHub](#aws-vpn-cloudhub)
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
     - [RDS Restore](#rds-restore)
     - [RDS Warnings](#rds-warnings)
     - [RDS Limits](#rds-limits)
     - [Multi-AZ Failover](#multi-az-failover)
- [DynamoDB](#dynamodb)
    - [Non-Ideal DynamoDB Scenarios](#non-ideal-dynamodb-scenarios)
    - [DynamoDB Integration](#dynamodb-integration)
    - [DynamoDB features](#dynamodb-features)
    - [Two ways to search](#two-ways-to-search)
- [ElasticCache](#elasticcache)
- [RedShift](#amazon-redshift)
    - [Architecture](#amazon-redshift-architecture)
        - [Leader Node](#leader-node)
        - [Computes Nodes](#computes-nodes)
    - [Backups and Fault Tolerance](#backups-and-fault-tolerance)
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
 ### VPC Peering
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
* Continuosly tracks changes and backups your database
* Volume snapshot of your entire DB instance, not just DB
* On day of backups retained by default but cand be configured up to 35 days
* Backup retention period defined during configuration
* When you delete an RDS instance, all automated snapshots are deleted. Manual snapshots are preserved
* Automated backups ocurr daily during a 30 minute configurable backup window
* Automated backups are preserved for a configurable number of days (retention period)
## RDS Restore
* RDS combines daily backups in conjuntion with transaction logs to restore the DB instance to any point during the retention period
## RDS Warnings
* You cannot restore from a DB snapshot to an existing DB instance
* Only default DB parameters and security groups are restored
## RDS Limits
* Up to the last five minutes, RDS uploads transaction logs for DB instances to Amazon S3 every 5 minutes. 
## Multi-AZ Failover
* Multi-AZ RDS deployment designed for HA
* Synchronous replication in a secondary AZ
* DB snapshots always taken against standby instance
* AWS automatically adjusts DNS records when needed
* Multi-AZ is different from a RDS read replica

# Amazon DynamoDB
* DynamoDB is a fully managed, highly available and scalable NoSQL database
* Automatically and synchronously replicates data across three AZ
* SSDs and limiting indexing on attributes provides high throughput and low latency
* ElasticCache can be used in front of DynamoDB
    * Offload high amounts of reads for non-frecuently changed data
* Ideal for existing or new applications that need:
    * A flexible NoSQL database with low read and write latencies
    * The ability o scale storage and throughput up or down as needed without code changes or downtime
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

# ElasticCache 
* Open-source in-memory caching engines
    * Memcached:
        * Widely adopted memory object caching system
    * Redis:
        * Popular open-source in-memory key-value store
        * Supports data structures such as sorted sets and lists
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

# Amazon RedShift 
* Fast and fully managed petabyte-scale relational data warehouse service.
* Analyze all your data using your existing bussines intelligence tools.
* HDD and SSD platforms.
* Starts at $0.25/hour
* Scale to $1000/TB/year
## Amazon RedShift Architecture
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
