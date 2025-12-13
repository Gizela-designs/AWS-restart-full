# NETWORKING
Under networking we had a few labs, i will show 2 labs i found challenging

# FIRST LAB: Create Subnets and Allocate IP addresses in an Amazon Virtual Private Cloud (Amazon VPC)
- Summarize the customer scenario

- Create a Amazon Virtual Private Cloud (Amazon VPC) and understand how to create subnets and allocate IP addresses

- Familiarize yourself with the Amazon Web Services (AWS) Management Console

- Develop a solution to the customer's issue in this lab

- Summarize and describe your findings (group activity)


![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/customerDiagram.PNG?raw=true)


## TTask 1: Investigate the customer's needs
Type and search for VPC

Launch VPC Wizard

Configure the following options:

For IPv6 CIDR block, leave No IPv6 CIDR Block selected. You will not be using IPv6 in this lab.

For the VPC name, enter First VPC

For Public subnet's IPv4 CIDR, this option prefills. Input the correct VPC CIDR that you are using; however, keep in mind that the public subnet's CIDR must be smaller then - the VPC CIDR block, and it must be able to include at least 50 IP addresses.

For Availability Zone, choose No Preference.

For Subnet name, leave this option set to Public subnet.

Leave the remaining options set to their default settings.

Create VPC.

![vpc](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/dashboard.PNG?raw=true)

![2](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/createVPC.PNG?raw=true)

![3](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/vpc3.PNG?raw=true)

![4](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/vpc4.PNG?raw=true)

![5](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/vpc5.PNG?raw=true)

![6](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/vpc6.PNG?raw=true)

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/networkingImages/WORKFLOW.PNG?raw=true)


## Task 2: Send the response to the customer

- Designed VPC layout and sized the CIDR block for all required IPs  
- Created separate public and private subnets to isolate resources by access level  
- Attached an Internet Gateway and updated route tables so only public subnets reach the internet  
- Left private subnets with local-only routes to keep them secure  
- Configured security groups and network ACLs to control inbound/outbound traffic  
- Tested subnet-to-subnet connectivity and verified expected reachability  
- Acted as both “customer” and “engineer” to see requirements from both sides  
- Gained end-to-end understanding of how subnets, routes, gateways, and security rules combine into a functional, secure cloud network


## WHAT I LEARNED

- I reviewed the customer’s problem to understand their networking needs and what kind of cloud environment they required
- I built an Amazon VPC and learned how to set up subnets and assign IP addresses, which is like designing separate network sections for different resources.
- I became familiar with navigating the AWS Console to manage networking, resources, and configurations more efficiently
- Using what I learned, I created a practical solution that addressed the customer’s requirements within the VPC


# Lab complete 🎓
## SECOND LAB: Build Your VPC and Launch a Web Server
Objectives After completing this lab, you should be able to:

- Create a virtual private cloud (VPC)
- Create subnets
- Configure a security group
- Launch an Amazon Elastic Compute Cloud (Amazon EC2) instance into a VPC

![diagram](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/networkingImages/customerDiagram.PNG?raw=true)

## Task 1: Create your VPC
I searched for "VPC" in the AWS Management Console and clicked "Create VPC." I configured the VPC settings and created it, then viewed the VPC details to confirm it was successfully created.


## Task 2: Create additional subnets
I navigated to the Subnets section and clicked "Create subnet." I created multiple subnets within my VPC to organize my network resources, repeating the process as needed.


## Task 3: Associate the subnets and add routes
I went to Route Tables and configured both public and private route tables. I associated the appropriate subnets with each route table and saved the associations to establish proper network routing.



## Task 4: Create a VPC security group
I selected Security Groups and created a new security group. I added inbound and outbound rules to control traffic, then saved the security group configuration.


## Task 5: Launch a web server instance
I navigated to EC2, selected Instances, and clicked "Launch instances." I configured the instance to run within my VPC, selected the appropriate subnet and security group, and launched the web server instance.



# WHAT I LEARNED
I learned how to build a complete cloud network environment by creating a VPC, structuring it with subnets, securing it with a security group, and launching an EC2 instance within it — essential steps for designing and deploying applications in AWS.

# Lab complete 🎓
