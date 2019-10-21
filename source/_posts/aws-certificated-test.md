---
title: aws certificated exam
date: 2019-10-21
tags:
---

## AWS Solution Architect Associate

Since I am preparing the the aws certification exam. This article is the note for the exam.

### What is AWS Certification Exam
AWS Certification helps learners build credibility and confidence by validating their cloud expertise with an industry-recognized credential, and organizations identify skilled professionals to lead cloud initiatives using AWS.

To learn more about the exam and prepare for it, you can access this link:

[AWS Certification Exam](https://aws.amazon.com/certification/certification-prep/)

### Solution Architect Associate

The level of the exam which I want to accept is the Solution Architect Associate.

The aim for this level is to ensure that you will have the essential knowleage to build a high aviable system.

[Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS_Certified_Solutions_Architect_Associate-Exam_Guide_EN_1.8.pdf)


The solution architcect associate contains several fileds.
- design system architecture with high resiliency.
- define high-performance architecture.
- secure application and architecture.
- cloud system with optimized cost.
- operational excellence.


### 1. abstract of aws service

###rchitected framework

Five points of the framework
- operational exellence
- security
- reliability
- performance and efficiency
- optimized cost 

#### AWS Infrastructure

- Region and Availbility Zone
Region in AWS means the region that seperated geographically, and Availbility Zone means the data center assembility in the AWS region.

- Edge location.
Service like Cloudfront or Route53. User can use the contents that are delivered from the nearby data center to gain low latency and high efficiency.

- Global Service : IAM、Route53、Cloudfront
  Region Service : VPC, Dynamo DB, Lambda
  Availbility Zone Service : EC2, RDS

- VPC(Virtual Private Cloud)
It is really important to set up a network environment that can only be acessed by the identified user for security. 
The corresponded service in AWS is the VPC.
VPC is used to build up an individual network space.

    - subnet
        A VPC is composed of several segment called subnet.
        The property of subnet must be defined when it is created(availbility zone it belongs to, network privacy - private/ public network)
    - internet gateway
       The gateway for the access from the inner resource in VPC to the internet.
    - route table
        static route defined for the instances in VPC subnet.
    - NAT Gateway
    NAT: Network address translattion. (Convert the global ip address to the ip address in private network or the inverted convertion)
    - Elastic IP
       service that providing the elastic fixed global IP address. Fee will not be caused when Elastic IP attached to the Running instance.
    - VPC Endpoint
      Two types of VPC endpoint.
        1. gateway type. It will access resource from the private network rather than the internet. The example is that using the target added to the route table to access the S3 or DynamoDB.
        2. interface type. AWS API called from the private network rather than from internet.
- Elastic Load Balancing(ELB)
    ELB is a load balancing service which is used to distribute the network traffic to EC2 or specific traffic.
    3 types of ELB
     - Classic load balancer(CLB)
        Providing standard load balancer. Distributing and transfering TCP requests to the backend instances.
     - Application load balancer(ALB)
        Based on the CLB, ALB provide service that distributes the request by the prepared path routing.
     - Network load balancer(NLB)
    
    The characteristics of ELB
    - high availablity.
    - auto scaling.
    - security
    - health check and monitoring