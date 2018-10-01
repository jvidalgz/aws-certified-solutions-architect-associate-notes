AWS Certified Solutions Architect  Associate -  Notes
=====================================
- [IAM](#iam)
    - [Features](#features)
    - [Accesing IAM](#accesing-iam)   
    - [Understanding How IAM Works](#understanding-how-iam-works)
    - [Overview of Identity Management: Users](#overview-of-identity-management:-users)
        - [First-Time Access Only](#first-time-access-only:-your-root-user-credentials)
        - [IAM Users](#iam-users)
        - [Federating Existing Users](#federating-existing-users)
    - [Overview of Access Management: Permissions and Policies](#overview-of-access-management:-permissions-and-policies)
        - [Policies and Accounts](#policies-and-accounts)
        - [Policies and Users](#policies-and-users)
        - [Policies and Groups](#policies-and-groups)
        - [Federated Users](#federated-users)
        - [Identity-based and Resource-based Policies](#identity-based-and-resource-based-policies)
    - [Warnings](#iam-warnings)
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
### IAM Warnings
* If a request to change some data is successful, the change is committed and safely stored. However, the change must be replicated across IAM, which can take some time. Such changes include creating or updating users, groups, roles, or policies. We recommend that you do not include such IAM changes in the critical, high-availability code paths of your application. 
* Policies and Users: Actions or resources that are not explicitly allowed are denied by default.
* You cannot attach a resource-based policy to an IAM identity.
