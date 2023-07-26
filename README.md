## Flexible IP Address Management Solution for AWS Control Tower

## Solution overview

Planning, tracking, and monitoring IP addresses for large-scale networks can challenging. Network Administrators often use a combination of spreadsheets, confluence pages, and home-grown tools to track IP address assignments across Amazon Virtual Private Clouds (Amazon VPCs), AWS Regions, and AWS accounts. However, these methods are largely manual and prone to errors, and even a minor mistake can cause IP address conflicts that can cause issues in establishing bidirectional connectivity.

This problem is amplified in large enterprise networks, where the AWS environment spans multiple AWS Organizational Units (OUs), AWS accounts, or even AWS Organizations. This is where Amazon VPC IP Address Manager (IPAM) comes in. IPAM simplifies IP address planning, tracking, and monitoring for your enterprise. With IPAM, you can release applications more quickly because developers don’t have to wait for the networking team to manage IP addresses. You can find overlapping IP addresses and fix them before issues arise with network connectivity. IPAM can notify you if your IP address pools are nearing exhaustion—it lets you quickly and efficiently perform routine IP address management activities.

If you combine IPAM with the power of Infrastructure-as-Code (IaC), then you can deploy IPAM across your environment quickly and in compliance with best practices. In this post, we describe a solution to turn on IPAM using AWS Service Catalog, and we walk you through it step-by-step. AWS Service Catalog uses AWS CloudFormation to abstract the underlying complexity and provides standardized deployments.

## Deployment instructions

The deployment of this Flexible IPAM solution consists of four steps:

### Phase 1: Deploy the AWS Service Catalog Portfolio in the Management Account

Step 1 – Create an S3 bucket to hold the Service Catalog Portfolio CloudFormation templates

Step 2 – Enable trusted access for AWS Service Catalog in Organizations

Step 3 – Deploy the Service Catalog Portfolios using CloudFormation

### Phase 2: Setup user access and provision the above created IPAM products using AWS Service Catalog ** 

Step 1 – Delegate an IPAM Administrator Account using the Delegate IPAM Product in your Management Account

Step 2 – Deploy the CloudFormation Macro definition using the IPAM CloudFormation Macro Product in your NetworkHub Account

Step 3 – Deploy the AWS Service Catalog IPAM Product in your NetworkHub Account

Step 4 – Deploy the Spoke VPC Product using the IPAM Spoke Product in your Spoke Account

## Authors

Mokshith Kumar - Senior Cloud Infrastructure Architect - tumallap@amazon.com

Raunak Tibrewal - Senior Product Manager - raunakt@amazon.com

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
