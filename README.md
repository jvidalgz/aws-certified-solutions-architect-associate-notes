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
    - [Placement Groups](#placement-groups)
    - [Warnings](#ec2-warnings)
    - [Limits](#ec2-limits)
- [Load Balancer](#load-balancer)
    - [Classic Load Balancer (CLB)](#classic-load-balancer-clb)
    - [Application Load Balancer (ALB)](#application-load-balancer-alb)
    - [Warnings](#lb-warnings)
- [Auto Scaling](#auto-scaling)
- [Elastic Block Storage (EBS)](#elastic-block-storage-ebs)
    - [Increasing IOPS Performance](#increasing-iops-performance)
    - [EBS-optimized instances](#ebs-optimized-instances)
    - [EBS Snapshots Characteristics](#ebs-snapshots-characteristics)
    - [EBS Snapshots Features](#ebs-snapshots-features)
    - [EBS Warnings](#ebs-warnings)
- [Elastic File System](#elastic-file-system-(efs))
    - [Limits](#efs-limits)
- [Simple Storage Service S3](#simple-storage-service-s3)
    - [S3 Features](#s3-features)
    - [Securing S3](#securing-s3)
- [Glacier](#glacier)
- [Storage Gateway](#storage-gateway)
- [CloudFront](#cloudfront)
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
### Placement Groups 
* A logical grouping of instances in a single availability zone
* Keep them as close as possible to each other in order to allow for low latency and high performance between these instances
* Can span peered VPCs (but not at full performance)
### EC2 Warnings
* Placement Groups: 
    * Can't span multiple availability zones
    * Reserved instances are supported on an instance level but you cannot explicity reserved CAPACITY for a placement group
    * You can't merge them 
### EC2 Limits
* The name must be unique (like S3 unique name convention) 
* Cannot be merged  

## Load Balancer
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

### EFS Limits 
* 1 to 1000 of EC2 instances, from multiple AZs, concunrrently
* By default, you can create up to 10 file systems per AWS account per region

## Simple Storage Service S3
### S3 Features
* File versioning
* Cross-region replication (CRR)
* Data lifecycle management 
* MFA Delete
* Permissions management
* Time-limited access to objects
### Securing S3
* Bucket policies
* MFA Delete
* Backing up your Bucket to another Bucket in a different account

## Glacier
* Integrates with Amazon S3 lifecycle policies
## Storage Gateway
* Gateway-cached volumes
* Gateway-stored volumes
* Gateway-virtual Tape Library (VTL)
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
