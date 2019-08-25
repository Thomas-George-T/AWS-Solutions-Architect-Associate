<h1 align="center"> AWS Solutions Architect Associate 2019</h1>
Materials & Resources aimed at acquiring the AWS Certified Solutions Architect Associate from an examination point of view. Work in Progress.

<p align="center">
  <br>
  <br>
  <a href="#">
    <img height=200 src="https://cdn.svgporn.com/logos/aws.svg">
  </a>
  <br>
</p>
<br>

## Table of Contents
* [Basic Overview](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#basic-overview)
  - [Edge Location](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#edge-location)
  - [Availability Zone](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#availability-zone)
  - [Region](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#region)
  
* [Identity Access Management (IAM)](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#identity-access-management-iam)
  - [Key features](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#key-features-of-iam)
  - [Key terminologies](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#key-terminologies-for-iam)
    - [Users](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#users)
    - [Groups](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#groups)
    - [Policies](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#policies)
    - [Roles](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#roles)
 
* [S3](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#S3)
  - [Basics](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#basics)
  - [Data Consistency](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#data-consistency)
  - [S3 Guarantees](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-guarantees)
  - [Features](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#features)
  - [Storage Classes](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#storage-classes)
    - [S3 Standard](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-standard)
    - [S3 – IA (Infrequently Accessed)](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3--ia-infrequently-accessed)
    - [S3 One Zone – IA](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-one-zone--ia)
    - [S3 – Intelligent Tiering](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3--intelligent-tiering)
    - [S3 - Glacier](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3---glacier)
    - [S3 Glacier Deep Archive](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-glacier-deep-archive)
  - [S3 Applicable Charges](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-applicable-charges)
  - [S3 Encryption](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-encryption)
  - [S3 Versioning](https://github.com/Thomas-George-T/AWS-Solutions-Architect-Associate#s3-versioning)

# Basic Overview

### Edge Location
Edge locations are endpoints for AWS which are used for caching content. Typically, this consist of CloudFront, Amazon’s Content Delivery Network (CDN)
### Availability Zone
An Availability zone is one or more discrete data centers, each with redundant power, networking and connectivity, housed in separate facilities.
### Region
A Region is a physical geographical location in the world which consists of two or more Availability zones (AZ’s).

**The number of Edge Locations > Number of Availability Zones > The number of Regions.**

# Identity Access Management (IAM)
IAM allows you manage users and their level of access to their AWS console.
* IAM is universal. It does not apply to all regions at this time.
* The **"root account"** is simply the account created when you first setup your AWS account. It has complete Admin access 
* New users have **NO permissions** when first created
* New users are assigned **Access Key ID** & **Secret Access Keys** when first created.
* **These are not the same as a password**. You cannot use the Access key ID & Secret Access key to Login into the console. You can use this to access AWS via the APIs and Command Line, however.
* **You only get to view these once**. If you lose the, you have to regenerate them. So, save them in a secure location.

## Key features
*	Centralized access to your AWS account
*	Shared access to AWS account.
* Granular Permissions.
*	Has Identity federation (Active directory, can connect with social media like Facebook, LinkedIn)
*	Multi Factor Authentication (MFA)
*	Provide temporary access to various users/devices and services where necessary.
*	Allows you to set up a password rotation policy.
*	Integrates with many different AWS services.
*	Supports PCI DSS Compliance


>What is PCI DSS Compliance?
>
>The Payment Card Industry Data Security Standard (PCI DSS) is a set of security standards designed to ensure that ALL companies that accept, process, store or transmit credit card information maintain a secure environment.
>

## Key Terminologies

### Users
End users such as people, employees of organizations etc.
### Groups
A collection of users. Each users of a group will inherit the permissions of the group.
### Policies
Policies are made up of Policy documents which are in JSON format and give permissions to what a User/Group/Role can do.
### Roles
Roles can be created to be assigned to AWS resources.

# S3
S3 provides developers and IT teams with secure, durable, highly scalable object storage. Amazons S3 is easy to use, with a simple web services interface to store and retrieve any amount of data from anywhere on the web.
*  S3 is safe place to store your files
* It is Object-based storage
* The data is spread across multiple devices and facilities
## Basics
* S3 is **Object based** - i.e. allows you to upload files
* Files can be from 0 bytes to 5 TB.
* There is unlimited storage.
* Files are stored in Buckets.
* **S3 is a universal namespace** -i.e. names must be unique globally.
* **Not suitable to install an operating system on.**
* When you upload a file to S3, you will receive a **HTTP 200 code** if the upload was successful.
* You can turn on **MFA Delete** 

By default, all newly created buckets are **PRIVATE**. You can setup access control to your buckets using:
* **Bucket Policies**
* **Access Control Lists**

S3 buckets can be configured to create access logs which log all requests made to S3 bucket. This can be sent to another bucket and even another bucket in another account.


__S3__ is Object based. **Think of Objects just as files** consisting of:
* Key (This is simply the name of the Object)
* Value (This is simply the data and is made up of a sequence of bytes)
* Version ID (Important for versioning)
* Metadata (Data about data you are storing)
* Sub resources
  - Access Control Lists
  - Torrent
  
## Data Consistency
* Read after Write consistency for PUTS of new Objects


If you write a new file and read it immediately afterwards, you will be able to view that data.
 
* Eventual Consistency for overview PUTS and DELETES (can take some time to propagate)


If you update **AN EXISTING FILE** or delete a file and read it immediately, you may get the older version, or you may not. Basically, changes to objects can take a little bit of time to reflect.

## S3 Guarantees
* 99.99% availability for S3 platform
* Amazon Guarantee 99.9% availability.
* Amazon guarantees 99.999999999 durability for S3 information (Remember 11 x 9s)
## Features
* Tiered Storage Available
* Lifecycle Management
* Versioning 
* Encryption
* MFA Delete
* Secure your data using **Access Control Lists** and Bucket Policies
## Storage Classes
There are 6 types of Storage Classes.
### S3 Standard 
99.99% availability.
99.999999999% durability, stored redundantly across multiple devices in multiple facilities, and is designed to sustain the loss of 2 facilities concurrently.
### S3 – IA (Infrequently Accessed)
For data that is accessed less frequently, but requires rapid access when needed. Lower fee than S3, but you are charged a retrieval fee.
### S3 One Zone – IA
For where you want a lower cost option for infrequently accessed data, but do not require the multiple Availability Zone data resilience.
### S3 – Intelligent Tiering
Designed to optimize costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
### S3 - Glacier
S3 Glacier is a secure, durable, and low cost storage class for data archiving. you can reliably store any amount of data at costs that are competitive with or cheaper than on premises solutions. Retrieval times configurable from minutes to hours.
### S3 Glacier Deep Archive
S3 Glacier Deep Archive is Amazon S3's lowest cost storage class where a retrieval time of 12 hours is acceptable.

| | S3 Standard | S3 Intelligent-Tiering | S3 - IA | S3 One Zone - IA | S3 Glacier | S3 Glacier Deep Archive |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Designed for durability | 99.999999999% (11 9's) | 99.999999999% (11 9's) | 99.999999999% (11 9's) | 99.999999999% (11 9's) | 99.999999999% (11 9's) | 99.999999999% (11 9's) |
| Designed for Availability | 99.99% | 99.99% | 99.99% | 99.5% | N/A | N/A |
| Availability SLA | 99.9% | 99% | 99% | 99% | N/A | N/A |
| Availability Zones | >=3 | >=3 | >=3 | 1 |  >=3 |  >=3 |
| Minimum capacity charge per object | N/A | N/A | 128KB | 128KB | 40KB | 40KB |
| Minimum storage duration charge | N/A | 30 days | 30 days | 30 days | 90 days | 180 days |
| Retrieval fee | N/A | N/A | per GB retrieved | per GB retrieved | per GB retrieved | per GB retrieved |
| First byte latency | milliseconds | milliseconds | milliseconds | milliseconds | select minutes or hours | select hours |  

## S3 Applicable Charges
* Storage
* Requests
* Storage Management Pricing
* Data Transfer Pricing
* Transfer Acceleration


**Amazon S3 Transfer Acceleration enables fast, easy and secure transfers of files over long distances between your end users and an S3 bucket.**


**Transfer Acceleration takes advantage of Amazon CloudFront's globally distributed  edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.**
* Cross Region Replication Pricing

## S3 Encryption
- Encryption in Transit is achieved by
	* **SSL/TLS**
- Encryption At Rest (Server Side) is achieved by
	* **S3 Managed Keys - SSE-S3**
	* **AWS Key Management Service, Managed Keys - SSE-KMS**
	* **Server Side Encryption With Customer Provided Keys - SSE-C**
- Client Side Encryption

## S3 Versioning
* Stores all version of an object (including all writes and even if you delete an object)
* Great backup tool.
* Once enabled, **Versioning cannot be disabled**, only suspended.
* Integrates with **Lifecycle** rules.
* Versioning's **MFA Delete** capability, which uses multi-factor authentication, can be used to provide an additional layer of security.

# Resources & Acknowledgements
* Ryan Kroonenburg - A Cloud Guru
