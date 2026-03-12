# Multi-AZ Fault-Tolerant VPC Infrastructure

This project uses **AWS CloudFormation** to deploy a highly available, three-tier network architecture.

## Architecture Highlights
* **VPC**: 10.0.0.0/16 CIDR block.
* **Multi-AZ**: Subnets distributed across two Availability Zones for high availability.
* **Security**: Web and App instances are located in private subnets.
* **Access**: No SSH keys required; access is managed via **AWS Systems Manager (SSM) Session Manager**.
* **NAT Gateways**: Allows private instances to securely access the internet for updates.

## How to Deploy
1. Upload `vpc-lab.yaml` to the AWS CloudFormation Console.
2. Wait for `CREATE_COMPLETE`.
3. Verify the web server by connecting via Session Manager and running `curl localhost`.