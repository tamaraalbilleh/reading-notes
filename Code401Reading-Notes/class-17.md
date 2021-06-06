# Readings: AWS: S3 and Lambda
## Review, Research, and Discussion

* Describe “The Cloud”
    * "The cloud" refers to servers that are accessed over the Internet, and the software and databases that run on those servers.

* What is a container (as it relates to computers and servers)?
    * A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. 

* What is auto-scaling?
    * AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.

* What is bandwidth?
    * Bandwidth describes the maximum data transfer rate of a network or Internet connection.

* How do cloud providers compute service costs?
    * The cost is calculated based on the resources the company or individual may use in the VM in order to run their apps/services smoothly. These recourses may be storage, processor, bandwidth and RAM.

## Document the following Vocabulary Terms

* Server Instances
    * A server instance is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. 

* Containers
    * is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. 
    
* Cloud Services
    * Cloud services are services available via a remote cloud computing server rather than an on-site server.

* Cloud Architecture
    * Cloud Architecture refers to the various components in terms of databases, software capabilities, applications, etc. engineered to leverage the power of cloud resources to solve business problems.

* AWS
    * Amazon Web Services, a (huge) collection of services that Amazon provide as a cloud computing, some of the AWS services are AWS EC2, Elastic Beanstalk and IAM 

* EC2/Beanstalk vs Heroku
    * Heroku is a cloud platform as a service supporting several programming languages.
    * EC2/Beanstalk : AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.

## Preparation Materials
### AWS S3
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. 
This means customers of all sizes and industries can use it to store and protect any amount of data for a range of use cases, such as data lakes, websites, mobile applications, backup and restore, archive, enterprise applications, IoT devices, and big data analytics.
### AWS Lambda Basics
AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS). Users of AWS Lambda create functions, self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient and flexible manner.

The Lambda functions can perform any kind of computing task, from serving web pages and processing streams of data to calling APIs and integrating with other AWS services.

Each Lambda function runs in its own container. When a function is created, Lambda packages it into a new container and then executes that container on a multi-tenant cluster of machines managed by AWS.

When building Serverless applications, AWS Lambda is one of the main candidates for running the application code. Typically, to complete a Serverless stack you’ll need:

* a computing service;
* a database service; and
* an HTTP gateway service.
### AWS Lambda Functions
AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster scaling logic, maintaining event integrations, or managing runtimes. With Lambda, you can run code for virtually any type of application or backend service - all with zero administration. 
### CDN
A Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content. A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos.
What does this mean for an SMB?
CDNs are something that larger companies are more likely to implement. The main reasons why company want to use CDNs are to improve Internet website load speeds, content delivery speeds, and to reduce the likelihood of falling victim to and improve defenses against Distributed Denial of Service attacks (DDoS).
 
A smaller company probably doesn’t need to improve website load speeds with a CDN as they typically don’t have an overwhelming amount of traffic. A Distributed Denial of Service attack may pose a potential threat against gambling companies or other mid-to-large enterprises such as banks or defense contractors. DDoS attacks are rarely used against SMB’s unless they upset a hacker group. CyberHoot is not saying a denial of service attack won’t happen, but the cost of protection is too much for most SMBs to afford.