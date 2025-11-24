# **Week 1: AWS Fundamentals**

## **What is AWS**

AWS stands for Amazon Web Services. It is Amazons cloud computing platform that allows you to rent computing power, storage, databases, and many other tools over the internet. Instead of buying physical servers and maintaining hardware, you simply use what you need and pay only for what you use.

### **The History of AWS**

- 2002: Amazon began experimenting with web based services
- 2006: AWS officially launched with its first major services including S3 for storage, EC2 for compute, and SQS for messaging
- The 2010s: Global growth increased rapidly as startups, enterprises, and governments adopted cloud services
- Today: AWS is one of the largest and most trusted cloud platforms in the world

---

## **Main AWS Service Categories**

AWS services can be grouped into several categories that help you build applications in the cloud.

### **Compute**

Services such as EC2 and Lambda provide processors and memory so you can run applications and websites. You can use virtual machines or choose fully serverless options.

### **Storage**

Tools including S3 and EBS help you store files, photos, logs, backups, and many other types of data. The storage is durable, scalable, and automatically backed up.

### **Databases**

Services like RDS for relational databases and DynamoDB for NoSQL databases make data management easier by handling much of the database maintenance for you.

### **Networking**

Your private cloud network is created using VPC. Services like CloudFront help you deliver content faster to users around the world.

### **Security**

IAM and KMS help you control who can access your resources and keep your information protected.

---

## **What is Cloud Computing**

Cloud computing simply means using computing resources that belong to someone else and are accessed over the internet. The cloud provider owns and maintains the physical hardware and you access the resources you need through the cloud.

### **Why Cloud Computing Matters**

No large upfront cost for hardware
You pay only for the resources you use
You can scale up or down instantly
You can access your systems from anywhere
No physical repair or maintenance is required

### **Types of Cloud Service Models**

IaaS or Infrastructure as a Service: You manage most things while AWS manages the underlying hardware. EC2 is a good example.
PaaS or Platform as a Service: AWS provides more of the environment and you focus mainly on your application. Elastic Beanstalk is an example.
SaaS or Software as a Service: You use a complete application without worrying about infrastructure. Gmail is an example.

---

## **The Shared Responsibility Model**

A good way to understand this model is to imagine renting an apartment.

### **AWS takes care of**

Physical security of data centers
Power, networking, and cooling
Maintenance of servers and infrastructure
Securing the overall global cloud platform

### **You take care of**

Your data
User access and permission settings
Your operating system updates
Application level security
Encrypting sensitive information

This model clearly identifies what AWS manages and what you manage.

---

## **AWS Pricing**

AWS uses a pay as you go billing system similar to paying for electricity. You are charged based on the amount of resources you use.

### **Main Pricing Approaches**

Pay as you go
Reserved pricing which gives discounts when you commit long term
Volume based discounts

### **AWS Free Tier**

The AWS Free Tier is designed for beginners and provides free usage of certain services for the first twelve months. It is very useful for learning and experimenting.

---

## **Amazon EC2 Virtual Servers**

EC2 means Elastic Compute Cloud. It is similar to renting a virtual computer inside an AWS data center. You can log into it and run anything including websites, databases, or data processing tasks.

### **Common Instance Types**

t2 micro which is small and part of the Free Tier
t2 medium which provides more balanced performance
c5 large which is optimized for CPU heavy tasks
r5 large which is optimized for memory heavy workloads

### **Pricing Options for EC2**

On Demand pricing gives flexibility and charges by the hour or second
Reserved Instances provide large discounts when committing for one to three years
Spot Instances offer the lowest cost by using extra AWS capacity

---

## **AWS Global Infrastructure**

AWS uses a worldwide network of data centers to deliver services to users everywhere.

### **Key Components**

Regions which are physical geographic locations
Availability Zones which are multiple data centers inside a region
Edge Locations which are points around the world where content can be cached for faster delivery

---

## **Week 1 Key Takeaways**

- AWS is Amazons cloud computing platform
- Cloud computing means using remote resources instead of owning hardware
- AWS pricing is based on pay as you go
- EC2 provides virtual servers in the cloud
- Security is split between you and AWS using the Shared Responsibility Model
- AWS uses Regions and Availability Zones for global availability
- You can learn using the Free Tier
- Cloud services follow the IaaS PaaS and SaaS models

---

## **Personal Note Rewritten Without Dashes**

This first week truly changed my perspective. Learning that entire servers, networks, and applications can be managed without ever touching physical hardware felt incredibly empowering. It showed me that anyone, no matter their background, can start building real technology systems just by learning how to use the cloud.

---
