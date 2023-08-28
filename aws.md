# AWS

### Your organization is using GitLab as a Version Control server. For AWS services compatibility, you suggested to migrate to a managed version control service in AWS.

CodeCommit.

### What is the relationship between an AZ (Availability Zone) and Region?

- The AZ is located in a Region
- The name of AZ is prefixed by the name of its Region

### Name some of the DB engines which can be used in AWS RDS
-MS-SQL DB
- MariaDB
- MYSQL DB
- OracleDB
- PostgreDB

### Suddenly, all the EC2 instances are terminated. How can you investigate the WHO and the WHEN of this issue ?
- Use AWS CloudTrail

### Your are deploying your static website to an S3 bucket. You are planning to automate this deployment while reducing the cost of this automation as much as possible. Which AWS services should you consider in this case?
- CodeBuild + CodePipeline

### What are the different types of Load Balancer in AWS services?
Two types of Load balancer are:
Application Load Balancer
Classic Load Balancer

### You developed an application that handles websocket sessions. Your application will be deployed in multiple EC2 instances to meet the demand. What AWS Load balancer type would meet those needs?

Application Load Balancer

### You deployed a Docker container registry system on an EC2 instance. The maintenance of this EC2 instance and its storage consumes your development time. Your manager asks you to come up with a solution that will save in time spent managing the application on the EC2 instance. What do you suggest?

- Migrate to Elastic Container Registry(ECR)

### An existing REST API application runs on-premise with a NGINX load balancer and sends traffic to servers that are running Java applications. You would like to move this application to the cloud with no changes to the code. What should you use?

Elastic Beanstalk

### An IAM policy document must contain at least three options. Tell me what is a options?
- Effect
- Resources
- Actions

### You deployed a NodeJS web application on an EC2 instance. This application exposes a REST API that searches on S3 files by name and metadata according to user query. Currently, the application does not have access to "s3://xp-videos" bucket where it performs the search. Hence, you attached an IAM Role to this EC2 instance and it remains the last step, which is attaching policies to that role. From the following policies, which one complies more with the principle of least privilege?

```
"Effect": "Allow",  "Action": ["s3:Get*", "s3:List*"], "Resource": ["arn:aws:s3:::xp-videos"]
```

### What are the advantages of auto-scaling?
Following are the advantages of autoscaling
Offers fault tolerance
Better availability
Better cost management


