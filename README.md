AWS Certified Solutions Architect  Associate -  Notes
=====================================
- [IAM](#iam)
    - [Features](#features)
    - [Accesing IAM](#accesing-iam)
    - [Warnings](#iam-warnings)
    - [Understanding How IAM Works](#understanding-how-iam-works)
    - [Overview of Identity Management: Users](#overview-of-identity-management:-users)
        - [First-Time Access Only](#first-time-access-only:-your-root-user-credentials)
        - [IAM Users](#iam-users)
        - [Federating Existing Users](#federating-existing-users)
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

### IAM Warnings
* If a request to change some data is successful, the change is committed and safely stored. However, the change must be replicated across IAM, which can take some time. Such changes include creating or updating users, groups, roles, or policies. We recommend that you do not include such IAM changes in the critical, high-availability code paths of your application. 
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
