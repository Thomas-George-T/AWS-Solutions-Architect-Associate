<h1 align="center"> AWS Solutions Architect Associate </h1>
Materials & Resources aimed at acquiring the AWS Certified Solutions Architect Associate. Work in Progress

<p align="center">
  <br>
  <br>
  <img src="https://cdn.svgporn.com/logos/aws.svg">
  <br>
  <br>
</p>

# Basic overview

### Edge Location
Edge locations are endpoints for AWS which are used for caching content. Typically, this consist of CloudFront, Amazon’s Content Delivery Network (CDN)
### Availability Zone
An Availability zone is one or more discrete data centers, each with redundant power, networking and connectivity, housed in separate facilities.
### Region
A Region is a physical geographical location in the world which consists of two or more Availability zones (AZ’s)
**The number of Edge Locations > Number of Availability Zones > The number of Regions.**

# Identity Access Management (IAM)
IAM allows you manage users and their level of access to their AWS console.
## Key features of IAM:
*	Centralized access to your AWS account
*	Shared access to AWS account.
*	Has Identity federation (Active directory, can connect with social media like Facebook, LinkedIn)
*	Multi Factor Authentication (MFA)
*	Provide temporary access to various users/devices and services where necessary.
*	Allows you to set up a password rotation policy.
*	Integrates with many different AWS services.
*	Supports PCI DSS Compliance

```
What is PCI DSS Compliance?
The Payment Card Industry Data Security Standard (PCI DSS) is a set of security standards designed to ensure that ALL companies that accept, process, store or transmit credit card information maintain a secure environment.
```

## Key Terminologies for IAM
### Users
End users such as people, employees of organizations etc.
### Groups
A collection of users. Each users of a group will inherit the permissions of the group.
### Policies
Policies are made up of Policy documents which are in JSON format and give permissions to what a User/Group/Role can do.
### Roles
Roles can be created to be assigned to AWS resources.

# Resources & Acknowledgements
* Ryan Kroonenburg - A Cloud Guru
