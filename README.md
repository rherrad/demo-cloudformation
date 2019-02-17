# Requirements

Use [00-network.yml](00-network.yml) to create a VPC with public and private subnets.  
[![Launch Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?#/stacks/new?stackName=demo-cloudformation-network&templateURL=https://s3-eu-west-1.amazonaws.com/sysless/demo-cloudformation/00-network.yml)

# Usage

Launch stack from [02-environment.yml](02-environment.yml) and specify parameters.  
[![Launch Stack](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?#/stacks/new?stackName=demo-cloudformation&templateURL=https://s3-eu-west-1.amazonaws.com/sysless/demo-cloudformation/02-environment.yml)

# Content

## [00-network.yml](00-network.yml)

- VPC
- Internet Gateway
- Route Table
- Private Subnets
- Public Subnets

## [01-application.yml](01-application.yml)

- Launch Configuration
- Auto Scaling Group
- Elastic Load Balancer

## [01-database.yml](01-database.yml)

- RDS Subnet
- RDS Instance

## [01-secret-rotation.yml](01-secret-rotation.yml)

- Secrets Manager rotation function from [serverless repository](https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:297356227824:applications~SecretsManagerRDSMySQLRotationMultiUser)
- Secrets Manager rotation schedule

## [02-environment.yml](02-environment.yml)

- Security Groups
- Secrets Manager Secret
- Application Stack
- Database Stack
- Secret Rotation Stack