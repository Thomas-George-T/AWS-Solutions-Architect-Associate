
## Notes

### Amazon Athena

Amazon Athena is an interactive query service that makes it easy to analyse data in Amazon S3, using standard SQL commands. 
It will work with a number of data formats including "JSON", "Apache Parquet", "Apache ORC" amongst others, but "XML" is not a format that is supported.

### Stateless services
1. RDS
2. DynamoDB
3. ElastiCache
4. Network Access Control lists (nACL)

### Stateful services
1. Elastic load balancer
2. Security Groups

### RDS

RDS database engines have a limit to the number of databases that can run per instance

>Both the Oracle and SQL Server database engines have limits to how many databases that can run per instance.
>Primarily, this is due to the underlying technology being proprietary and requiring specific licensing 
>to operate. The database engines based on Open Source technology such as Aurora, MySQL, MariaDB 
>or PostgreSQL have no such limits.

### Encryption at Rest

* **EBS**, **S3** and **EFS** all allow the user to configure encryption at rest using either the AWS Key Management Service (KMS) or, in some cases, using customer provided keys. 

* **Elasticache** for **Redis** offers a native encryption service but Elasticache for Memcached does not.

* For **EC2**, encryption at rest can be achieved by:
	1. Using third party volume encryption tools
	2. Encrypting your data inside your application, before storing it on EBS.
	3. Encrypting the data using native encryption tools available in the operating system (such as Windows BitLocker)
	
### EC2
 
Hypervisors used are:
1. Nitro
2. Xen
3. KVM

### Four levels of AWS premium
1. Basic
2. Developer
3. Business
4. Enterprise

### AWS Trusted Advisor

- Trusted Advisor inspects your AWS environment, and then makes recommendations when opportunities exist to save money, improve system availability and performance, or help close security gaps. 
- All AWS customers have access to five Trusted Advisor checks.

## Useful Resources

### S3

- [S3 Pricing](https://aws.amazon.com/s3/pricing/)

### DynamoDB

- [Request & Response Formats](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Programming.LowLevelAPI.html#Programming.LowLevelAPI.RequestFormat)

### SAML

- [Enabling SAML for your AWS resources](https://aws.amazon.com/identity/saml/)

### Auto Scaling

- [Default Termination policy](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html)

### CloudFormation

- [Template Anatomy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-anatomy.html)

## User Guides

- [DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html)

- [AWS WAF, AWS Shield, AWS Firewall Manager](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)

- [AWS Macie](https://docs.aws.amazon.com/macie/latest/userguide/what-is-macie.html)

- [AWS Support Plans](https://docs.aws.amazon.com/awssupport/latest/user/getting-started.html)

- [AWS Trusted Advisor](https://docs.aws.amazon.com/awssupport/latest/user/getting-started.html#trusted-advisor)

## FAQ Links

- [DynamoDB](https://aws.amazon.com/dynamodb/faqs/)

- [Storage Gateways](https://aws.amazon.com/storagegateway/faqs/)

- [EC2](https://aws.amazon.com/ec2/faqs/)

## White papers

- [AWS Security Best Practice](https://aws.amazon.com/blogs/security/new-whitepaper-aws-cloud-security-best-practices/)
- [AWS Cloud Best Practice](https://d0.awsstatic.com/whitepapers/AWSCloudBest_Practices.pdf)