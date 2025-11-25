# AWS Cloud Quest 🎮  

# What I Did in Cloud Quest:
# Cloud Computing Essentials ☁️💡
I learned the foundational ideas behind Cloud Computing and gained a solid understanding of what AWS really is. I discovered how the cloud operates, why businesses prefer it instead of purchasing their own physical servers, and the major advantages it offers, including reduced costs and the ability to scale easily. I explored the AWS Management Console and became familiar with navigating the different services that AWS provides. This helped me realize that the cloud is simply a collection of powerful computers owned by someone else and made available for us to rent through the internet.


# My First Steps 👣
took my first real steps in AWS by creating and launching my first EC2 instance, better known as a virtual server. I learned how to choose the right size server, pick an operating system, and configure the basic settings. I connected to my server using SSH and ran some commands to make sure everything was working. This taught me that starting a server in the cloud only takes minutes, not weeks like traditional data centers. I also learned to stop and start instances in order to save money.

# Computing Solutions 💻
I spent time learning how to match different problems with the correct types of EC2 instances. I now understand the differences between general purpose, compute optimized, and memory optimized instances, and I practiced choosing the right one for specific workloads. For example, I saw how a strong CPU based instance is better for heavy calculations, while a memory focused instance works best for databases or applications that need a lot of RAM. I also explored the various pricing options such as On Demand, Reserved, and Spot instances so I can choose the most cost effective option depending on the situation.

# Networking Concepts 🔌
I learned the fundamentals of networking in AWS and even created my first VPC. I now understand what IP addresses are and the difference between public and private IPs. I also learned how subnets divide a network into smaller sections and how CIDR notation such as slash twenty four shows the size of a subnet and how many devices it can hold. I explored the basics of routing as well and gained an understanding of how data moves from one location to another through routers and gateways.

# Connecting VPCs 🔗
I worked on connecting multiple VPCs so they could communicate with each other. I learned how VPC peering creates a private connection between two VPCs without using the internet, allowing them to share resources securely. I configured route tables so traffic could move correctly between the VPCs and adjusted security groups to make sure the right connections were allowed. This helped me understand how large companies link different departments or regions inside AWS while keeping all communication secure and private within the AWS network.

# Cloud Economics 📊
I learned how to calculate and optimize cloud costs. I used the AWS pricing calculator to estimate monthly expenses before building anything, which helped me understand how different choices affect the final bill. I explored several cost optimization strategies, such as choosing Reserved Instances for long term stable workloads, using Spot Instances for flexible tasks, and right sizing instances so I do not pay for resources I am not actually using. I also learned about the AWS Free Tier and how to set up billing alarms to avoid unexpected charges. This experience showed me that managing costs is just as important as designing and building cloud solutions.

# Databases in Practice 🗄️💾
I built my first relational database on Amazon RDS. I learned the difference between having my own database on EC2 and using RDS, where AWS handles backups, updates, and maintenance automatically for me. So I configured database settings like storage size, backup retention, and multi-AZ deployment for high availability. I then connected an application to the database and practiced storing and retrieving data. This taught me that managed databases save a ton of time and effort.

# First NoSQL Database 📦🚀
I created my first NoSQL database using Amazon DynamoDB. I learned that NoSQL databases differ from the traditional SQL ones; they are faster, more flexible, and better for specific use cases, such as mobile apps or gaming. I created tables, put items within them with different attributes, and queried data. I found out about such concepts as partition keys, sort keys, and how DynamoDB scales itself automatically to sustain millions of requests. It showed me that not all data needs to be in the traditional table format.

# File Systems in the Cloud 📁
I worked with several storage services in AWS and learned how each one is used. I used Amazon S3, the Simple Storage Service, to store files such as images, videos, and backups. I discovered that S3 is an object storage service that is extremely durable and very cost effective. I also explored Amazon EFS, the Elastic File System, which works like a shared network drive that many EC2 instances can access at the same time. I learned when each storage type is most suitable, using S3 for static files and backups, EBS for server level hard drives, and EFS for files that need to be shared across multiple servers.

# Core Security Concepts 🛡️
I learned the fundamental security practices in AWS. I worked with IAM-Identity and Access Management-to create users, groups, and roles with specific permissions, giving access to only those resources that are needed. I have configured the security groups-virtual firewalls-to control who can access my servers and on which ports. I learned about encryption for data at rest and in transit, and why we should never share access keys or passwords. This taught me that security must be built in from the start, not added later.

# Auto Healing and Scaling Applications 📈
I created automatic healing and scaling of my application. I learned the use of Auto Scaling Groups that add servers automatically when traffic increases and remove them when traffic decreases so I will pay only for what I use. I configured health checks that detect server failures automatically and replace them with new ones without human intervention. Besides, I set up alarms in CloudWatch to monitor performance and scale accordingly. That showed me how the cloud could make applications self-managing and resilient.

# Highly Available Web Applications 🌐
I built a complete, highly available web application that can survive server failures. I used servers deployed across multiple Availability Zones such that if one data center goes down due to problems, my app will remain running in another. I also configured an Elastic Load Balancer to equally distribute traffic between multiple servers and automatically route around failed ones. I then combined this with Auto Scaling Groups, RDS Multi-AZ databases, and S3 for static files to create a fully redundant system. This final quest has taught me how to architect professional, enterprise-grade applications that stay online 24/7 even when things go wrong

# 🎓 What I Learned:
I began this journey knowing nothing about cloud computing, but through the twelve quests in this class I learned how to build secure, scalable, cost optimized, and highly available applications on AWS. I realized that the cloud is not just about technology but about creating smarter, faster, and more reliable solutions than traditional IT ever could. I now understand what the core AWS services do, how to apply best practices for security and cost management, and how to design applications that can handle real world demands. Completing this course gave me practical, hands on experience that I can confidently use in real cloud projects.✨

