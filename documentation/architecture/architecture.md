# System Architecture

## Proposed Architecture

The Youth Support Directory will use cloud infrastructure to host the application, store service information and monitor the system.

The initial architecture will explore the following components:


                         USER
                           │
                           ▼
                    Web Application
                           │
                           ▼
                    AWS Cloud Environment
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
          Amazon EC2                Amazon S3
       Application Hosting        Object Storage
              │
              ▼
          Amazon RDS
           Database
              │
              │
              ▼
         Amazon CloudWatch
           Monitoring

              │
              ▼
             IAM
      Access & Permissions

              │
              ▼
             VPC
       Network Environment

## AWS Components

### Amazon EC2

EC2 will be explored as a potential hosting environment for application components.

### Amazon S3

S3 will be explored for storing static files and other appropriate project assets.

### Amazon RDS

RDS will be explored as the managed relational database for storing information about support organisations and services.

### IAM

IAM will be used to manage access to AWS resources and explore least-privilege access.

### Amazon VPC

The application infrastructure will operate within an AWS networking environment using VPC concepts such as subnets, routing and security groups.

### Amazon CloudWatch

CloudWatch will be explored for monitoring application and infrastructure performance.

### Terraform

Terraform will eventually be used to explore Infrastructure as Code and automate the creation of selected AWS resources.

## Data Flow

The expected basic flow is:

User
↓
Application
↓
Application processes search request
↓
Database queried
↓
Relevant services returned
↓
User views service information

## Security Considerations

The project will follow basic security principles, including:

- Least-privilege access
- Secure credentials
- Restricted network access
- Avoiding unnecessary collection of personal information
- Protecting database access
- Monitoring infrastructure

## Architecture Status

This is a proposed architecture.

The architecture may change as the project is implemented and as additional AWS concepts are learned.
