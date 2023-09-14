# AWS Cloud Practitioner Notes

## Index
1. [Cloud concepts](#cloud-concepts)
    - [Cloud computing models](#cloud-computing-models)
      - [IaaS](#iaas)
      - [PaaS](#paas)
      - [SaaS](#saas)
    - [Cloud computing deployment](#cloud-computing-deployment)
      - [Benefits ](#benefits-)
      - [Cloud deployment (Public cloud)](#cloud-deployment-public-cloud)
      - [On-premises deployment (Private cloud)](#onpremises-deployment-private-cloud)
      - [Hybrid deployment (Hybrid Cloud)](#hybrid-deployment-hybrid-cloud)
    - [Well-Architected Framework](#wellarchitected-framework)
    - [Six Advantages of Cloud Computing](#six-advantages-of-cloud-computing)
    - [AWS Services by Group](#aws-services-by-group)
2. [Security and Compliance](#security-and-compliance)
    - [Security in the Cloud](#security-in-the-cloud)
      - [Shared Responsability Model](#shared-responsability-model)
      - [Security Pillar of the Well-Architected Framework](#security-pillar-of-the-wellarchitected-framework)
      - [Principle of the Least Privilege](#principle-of-the-least-privilege)
      - [AWS Cloud Compliance](#aws-cloud-compliance)
    - [IAM (Identity and Access Management)](#iam-identity-and-access-management)
      - [Manage Users](#manage-users)
      - [IAM Roles](#iam-roles)
      - [Federated Users](#federated-users)
    - [AWS Security Services](#aws-security-services)
3. [Technology](#technology)
    - [Compute](#compute)
      - [EC2](#ec2)
      - [Elastic Beanstalk](#elastic-beanstalk)
      - [Elastic Load Balancing](#elastic-load-balancing)
      - [AWS Lambda](#aws-lambda)
      - [Lightsail](#lightsail)
      - [AWS Global infrastructure](#aws-global-infrastructure)
    - [Storage](#storage)
      - [S3](#s3)
      - [Elastic Block Store](#elastic-block-store)
      - [Snowball](#snowball)
      - [Storage Gateway](#storage-gateway)
    - [Database](#database)
      - [DynamoDB](#dynamodb)
      - [RDS](#rds)
      - [Aurora](#aurora)
      - [Redshift](#redshift)
    - [Network and Content Delivery](#network-and-content-delivery)
      - [VPC](#vpc)
      - [CloudFront](#cloudfront)
      - [Route53](#route53)
    - [Management Tools](#management-tools)
      - [CloudFormation](#cloudformation)
      - [CloudTrail](#cloudtrail)
      - [CloudWatch](#cloudwatch)
4. [Billing and Pricing](#billing-and-pricing)
    - [Billing and cost management dashboard](#billing-and-cost-management-dashboard)
    - [Pay-As-You-Go Model of Cloud Computing](#payasyougo-model-of-cloud-computing)
      - [Fundamental drivers of cost](#fundamental-drivers-of-cost)
        - [Compute](#compute)
        - [Storage](#storage)
        - [Outbound Data Trnasfer](#outbound-data-trnasfer)
    - [Consolidated Billing](#consolidated-billing)
    - [Cost Calculators](#cost-calculators)
      - [Total Cost of Ownership (TCO) Calculator](#total-cost-of-ownership-tco-calculator)
      - [AWS Princin Calculator](#aws-princin-calculator)
      - [Part of Billing and Cost Management Console](#part-of-billing-and-cost-management-console)
      - [AWS Free Tier](#aws-free-tier)
    - [Support Plans](#support-plans)
      - [Basic](#basic)
      - [Developer](#developer)
      - [Business](#business)
      - [Enterprise On-Ramp](#enterprise-onramp)
      - [Enterprise](#enterprise)

## Cloud concepts

### Cloud computing models

#### IaaS
- Basic building blocks
- Most flexibility and management control
- Closest to having a traditional on-premises data center

#### PaaS
- Deploy and manage applications without worry
- Execute programming languages to gost applications
- Less flexibility than IaaS, as packages are preconstructed

#### SaaS
- completed products managed by the service provider
- easy to use as end user
- Least flexibility

### Cloud computing deployment

#### Benefits 
<img src="./Cloud Computing Model Benefits.png">

#### Cloud deployment (Public cloud)
- 100% of IT infrasctructure on the cloud
- All aplications migrated ti ir created in the cloud
- Removes roadblock of costly and time-consuming procurement process

#### On-premises deployment (Private cloud)
- Use virtualization to deploy respources in their on-premises data centers
- Often looks like traditional IT infrastructure
- Does not provide a lot of benefits of cloud computing
- Resources cannot be accessed using the internet
- Security: Provides dedicated resources

#### Hybrid deployment (Hybrid Cloud)
- Connects on-premises technology with cloud based resources
- Great for established companies that are in the process of migrating over the cloud
- Data partially on the cloud and partially in the on-premises data center
- Can use as backup and disaster recovery solution

### Well-Architected Framework
1. Cost optimization
2. Relaiability
3. Operational excellence
4. Performance efficienty
5. Security
6. Sustainability

### Six Advantages of Cloud Computing
1. Trade capital expense for variable expense
2. Benefit from masive economies of scale
3. Stop guessing about capacity
4. Increase speed and agility
5. Stop spending monet running and mantaining data centers
6. Go global in minutes

### AWS Services by Group
<img src="./AWS Service Groups.png">

## Security and Compliance

### Security in the Cloud

#### Shared Responsability Model
- Customer: responsible for security in the cloud
- AWS: resposible for security of the cloud
- Security of data and resources in the cloud is a shared responsability between the cloud computing service provider and the customer

#### Security Pillar of the Well-Architected Framework
- Idendity and access management
- Detective Controls
- Infrastructure Protection
- Data Protection
- Incident Response

#### Principle of the Least Privilege
- Only provide access to resources an entity requires to do its job
- Permission should be no more or no less than the optimal level of access
- Use IAM (Identity and Access Management) in the AWS Cloud
- Coincides with the shared responsability model

#### AWS Cloud Compliance
- Visit https://aws.amazon.com/compliance to review the different compliance programs

### IAM (Identity and Access Management)
- Manage access to services and resources on the AWS cloud
- Manage users and groups
- Can provide access to users or other AWS services
- Permissions are global: any access setting will be true across all regions
- Follow priniciple of least privilege

#### Manage Users
- Create users in IAM and assign them security credentials
- Users can have very precise permissions sets
- User can access AWS through AWS management console
- You can provide programmatic access to data/resources
- Programmatic access: applications directly accessing resources instead of huma doing the same activity

#### IAM Roles
- Create roles to manage permissions and what those roles can do
- An entity assumes a role to obtain temporary security credentials to make API calls to your resources
- Used to priovide access to a user from another AWS account to your AWS account

#### Federated Users
- Enable identity federation: allow exisitng identities in your enterprise to access AWS without having to create IAM user for each identity, ideal for lists
- Can use any identity management solution using SAML 2.0 or one of AWS federation samples

### AWS Security Services
- IAM Identity and Access Management
  - Manage permissions and create users, roles and federated users
- AWS Web Application Firewall (WAF)
  - Firewall for for web applications
- AWS Shield
  - Protects against DDoS attacks
- Amazon Inspector
  - Find potetntial vulnerabilities
- AWS Trusted Advisor
  - Provides advice on cost optimization, performance, security, fault tolerance, service limits
- Amazon GuardDuty
  - Threat detection service 24/7

## Technology

### Compute

#### EC2
- Vistual server hosted onAWS Cloud
- Instantly launch applications and servers whenever you want
- Extremely versatile
- One of the most widely used services in AWS

#### Elastic Beanstalk
- Deploy and scale web applications by uploading code
- Handles the deployment process like capacity provicioning, load balancing, auto-scaling and application health monitoring
- Can upload in many popular programming languages
- Remain full control of the underlying resources at all times

#### Elastic Load Balancing
- Help web application achieve fault tolerance
- Ensure scalability, performance, and security
- Monitor health servers and when one goes down, reroute incoming traffic to healthy servers
- Highly available, secure, flexible and monitorable

#### AWS Lambda
- Runs code ("Lambda functions") in response to an event
- No servers to provision manage or scale
- The functions only runs in response to an event so you only pay for the time the code spends running, saving you money

#### Lightsail
- Preconfigured and ready to use operative systems, web applications and development stacks
- Scalable and simple to spin up virtual services

#### AWS Global infrastructure
- Two or move Availability zones (Independent data centers) make up a region
- AWS cloud infrastructure is generaly hosted in aregion closes to you organization's physical location
- Create redundancy (replace resources in AZs and regions) to create highly available and resilient IT infrastructure on the AWS cloud

### Storage

#### S3
- Object storage serivce
- Designed for scalability, data availability, security, and performance
- Many storage classes available to fit budget and needs  
- Set up S3 lifecycle policies to automatically transfer files from one storage class to a cheaper one after a certain number of days (like Glacier)

#### Elastic Block Store
- Block storage service
- Behaves like raw, unformatted block devices
- Can be attached to EC2 instances to expand storage capacities
- Scalable, durable and reliable storage option

#### Snowball
- Ona of vary few hardware AWS services (a physical device)
- Data migration tool that can function as storage device
- AWS Physically ships you a "Snowball" to move data onto and mail back
- AWS uploads the mailed back data onto AWS S3
- Faster to upload to the cloud than using your internet

#### Storage Gateway
- Hybrid storage solution for your IT infrastructure
- Provides low latency for file access while also providing benefit of cost and time savings by leveraging cloud computing
- Is a "gate" thhat connects your onsite users and devices to resources stored in the AWS Cloud with minimal latency
- Three types: File Gateway, Tape Gateway, and Volume Gateway

### Database

#### DynamoDB
- Fast, flexible, fully managed and secure
- Non relational DB
- Serverless - you dont have to provision patch or manage servers
- Automatically scales up or down to adjust to your needs

#### RDS
- Fully managed relational database
- Highly scalable
- Six database engines to choose from
  - Amazon Aurora
  - PostgresSQL
  - MySQL
  - MariaDB
  - Oracle Database
  - SQL Server
- Databases up to 64 TB of space

#### Aurora
- One of six relationaldatabases supported by Amazon RDS
- Fully managed by RDS no administration or provisioning necessary
- PostgresSQL and MySQL compatible
- Auto-scaling

#### Redshift
- Fully managed, petabyte-scale fata warehouse service
- Super fast, super cheap
- You pay for what you use
- Fully integrated with your data lakes
- Encription compliance with industry regulations

### Network and Content Delivery

#### VPC
- Isolated corner of AWS cloud made for you at account creation
- Provision AWS resources into a private virtual network that you define
- Have complete control over the environment and security

#### CloudFront
- Content delivery network (CDN) makes websites and applications load faster
- Uses Edge Locations all around the world to cache resources for quick retrieval by usesr close to the Edge Locations
- Sees where the user is based adn routes their traffic to the closes cached location to have the quickest loading time

#### Route53
- Highly scalable domain name sistem (DNS)
- Route users to your internal applications
- Basic functions: domain registration, DNS, health checking of web applications, accesibility, and auto-naming for service discovery

### Management Tools

#### CloudFormation
- Create a recipe for spinning up identical sets of resources as services
- Utilizes infrsastructure as code. Deploy IT infrstructure based on a text file written in code that specifies coinfigurations for services and resources
- Remove human error from manual setups
- Save time

#### CloudTrail
- Logs and monitors account activities
- Provides event history of account activities; visibility into user and resource activities
- Simplify compliance audits
- Discover and troubleshoots security and operational issues
- Tracks automatically responds to security threat

#### CloudWatch
- Gain system-wide visibility into resource utilization, application performance and operational health
- Collects monitoring and operational data as logs, metrics, and events
- Provide insights into application performance
- Set up CloudWatch alarms to automatically make changes using preconfigured triggers to automatically solve common issues

## Billing and Pricing

### Billing and cost management dashboard
- Estimate and plan you AWS costs
- Consolidated billing: sinple accounting for multiple AWS account withtin your organization
- Alert you when you're nearing usage threashholds which could mean additional costs
- Use cost explorer to view costs as graphs

### Pay-As-You-Go Model of Cloud Computing
- No huge upfront costs
- Billed only for the resources consumed
- Easily scale resources up or down to suit business needs

#### Fundamental drivers of cost

##### Compute
- Pay hourly from the time launched to termination
  - EC2 (virtual server): Pay for length of time the server is up and running

##### Storage
- Pay per GB of storage used
  - S3 (storage service): Upload photos into an app and pay for the storage used

##### Outbound Data Trnasfer
- Pay to transfer data out of AWS
  - Usually no charge for data into AWS or data transfers between other AWS services (in other words, between S3 and EC2) within the same region

### Consolidated Billing
- Create a payer account that views and pays combined billing charges for all linked accounts
- Independent account, but can't use any other services
- Cannot deploy services into the linked accounts
- All resource usage becomes consolidated as usage from one large entity - organization may be eligible for volume discounts

### Cost Calculators

#### Total Cost of Ownership (TCO) Calculator
- Get teports on estimated savings from moving on-premises IT infrastructure onto AWS cloud
- Total cost of Ownership (TCO) includes upfront hardware infrastructure costs and mantainance costs
- TCO can be reduced by moving to the cloud because no upfront infrastructure purchases
- Pay-As-You-Go model: pay only when your business uses the resources
- https://awstcocalculator.com

#### AWS Princin Calculator
- Estimate cost of lcoud architecture solution you want to build
- Add services and calculator to the calendar to get a report of estimated costs per service, service group and total infrastructure
- Compare service costs per region, reduce EC2 spend, find the right EC2 instance to fit your needs or estimate overall AWS cloud spend
- https://calculator.aws.com

#### Part of Billing and Cost Management Console
- Located in Billing and Cost MAnagement console
- View and analyze your AWS cloud costs and usage
- Forecast how much you're likely to spend in upcoming month
- Get recommendations for wha reserved instancens to purchase to minimize costs

#### AWS Free Tier
- Always free plan
- 12 Months free plan

### Support Plans
- AWS support plans:
  - https://aws.amazon.com/premiumsupport/plans

#### Basic
- No tech support; customer service limited to account and billing questions
- AWS community forums
- Seven core Trusted Advisor checks
- AWS PErsonal Health Dashboard

#### Developer
- Cost: $29/mo OR 3% of monthly AWS usage bill (whichever is higher)
- One primary contact to sybmit tech support requests
- Unlimited number of cases
- Technicians will respond during business hours via email
- Service-level agreement (SLA) for response: 12 hours for impaired system, 24 hours for general guidance

#### Business
- Cost: $100/mo OR 3-10% of monthly AWS usage bill (whichever is higher)
- Unlimited number of contacs can open unlimited number of support cases
- Access AWS Support API for support case automation
- Retrieve detailed information about support operations and data types in JSON format
- Full acces to AWS Trusted Advisor checks
- Can retrieve Trusted Advisor check data throught AWS Support API
- Access to Infrastructure Event Management (extra fees)
- Third-party application integration support
- SLA 24/7 support via phone, email, and chat
- One-hour response time for urgent support cases when production system is down

#### Enterprise On-Ramp
- Cost: $5.500 per month or 3-10% of monthly AWS usage bill (whichever is higher)
- Consolidative application architecture guidance on how AWS resources can meet unique use case
- Short-term engangement with AWS Support for architectural and scaling guidance for infrastructure Event MAnagement
- Access to pool of Techincal Account Managers (TAMs) and Concierge Support Team
- Access to management business reviews
- SLA 24/7 support via phone, email, and chat
- 30 minutes response time for business-critical system down

#### Enterprise
- Cost: $15.000 per month or 3-10% of monthly AWS usage bill (whichever is higher)
- 24/7 tech support with service level agreement (SLA) of 15 minutes for emergencies
- Access to pool of Techincal Account Managers (TAMs) and Concierge Support Team
- Free proactive maintainance programs, well-architected reviews, and training amongst other features
- For huge organizations with huge budgets and mission-critical resources on AWS Cloud
