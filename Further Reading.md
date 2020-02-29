
Amazon Athena

Amazon Athena is an interactive query service that makes it easy to analyse data in Amazon S3, using standard SQL commands. 
It will work with a number of data formats including "JSON", "Apache Parquet", "Apache ORC" amongst others, but "XML" is not a format that is supported.

Stateless services:
1. RDS
2. DynamoDB
3. ElastiCache

Stateful services:
1. Elastic load balancer

RDS

RDS database engines have a limit to the number of databases that can run per instance

	Both the Oracle and SQL Server database engines have limits to how many databases that can run per instance. Primarily, this is due to the underlying technology being proprietary and requiring specific licensing to operate. The database engines based on Open Source technology such as Aurora, MySQL, MariaDB or PostgreSQL have no such limits.

Encryption at Rest

EBS, S3 and EFS all allow the user to configure encryption at rest using either the AWS Key Management Service (KMS) or, in some cases, using customer provided keys. 

Elasticache for Redis offers a native encryption service but Elasticache for Memcached does not.

FAQ Links

DynamoDB
https://aws.amazon.com/dynamodb/faqs/

Storage Gatways
https://aws.amazon.com/storagegateway/faqs/

Useful Resources

DynamoDB

1. Request & Response Formats
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Programming.LowLevelAPI.html#Programming.LowLevelAPI.RequestFormat

SAML

1. Enabling SAML for your AWS resources
https://aws.amazon.com/identity/saml/

Auto Scaling
Default Termination policy
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html

Developer Guides

1. DynamoDB 
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Introduction.html

White papers
AWS Security Best Practice