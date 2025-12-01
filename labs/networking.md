# NETWORKING
Under networking we had a few labs, i will show 2 labs i found challenging

# Internet Protocols - Public and Private IP addresses
 
## Objectives
In this lab, you will:

- Summarize and investigate the customer scenario
- Analyze the difference between a private and public IP address
- Develop a solution to the customer's issue in this lab

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/networkingImages/customerDiagram.PNG?raw=true)


## Task 1: Investigate the customer's needs
- Type and search for VPC

- Launch VPC Wizard

- Configure the following options:

- For IPv6 CIDR block, leave No IPv6 CIDR Block selected. You will not be using IPv6 in this lab.

- For the VPC name, enter First VPC

- For Public subnet's IPv4 CIDR, this option prefills. Input the correct VPC CIDR that you are using; however, keep in mind that the public subnet's CIDR must be smaller then - the VPC CIDR block, and it must be able to include at least 50 IP addresses.

- For Availability Zone, choose No Preference.

- For Subnet name, leave this option set to Public subnet.

- Leave the remaining options set to their default settings.

- Create VPC.


![vpc](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![2](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![3](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![4](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![5](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![6](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)




## **Task 2: Response to the Customer – Student-Friendly Version**

For this task, I acted as both the customer and the cloud technician. I started by planning what the VPC should look like and chose a CIDR block that would give enough IP addresses for all the subnets. After that, I created a public subnet and a private subnet so that different resources could be placed where they fit best. Public subnets are for resources that need internet access, and private subnets are for the ones that should stay inside the network.

Once the subnets were created, I set up the routing. The public subnet was connected to an internet gateway so it could reach the internet, while the private subnet stayed isolated for security. I configured security groups and network ACLs to control what kind of traffic is allowed to move in and out of the VPC.

During the process, I tested communication between the subnets to make sure everything could connect the way it should. Completing all of this by myself helped me fully understand how subnets, route tables, gateways, and security settings all work together in a VPC. It also taught me how to think from both a customer’s perspective and an engineer’s perspective, which is important when designing cloud solutions.

---

## **What I Learned**

While working through this lab, I learned how to read and understand a customer’s problem so that I could decide what kind of cloud environment they needed. I learned how to build a VPC, create subnets, and assign IP addresses. This felt similar to designing different rooms inside a building so everything has its proper place. I also became more comfortable navigating the AWS Console and changing settings for networking and resources. Using everything I learned, I was able to build a working VPC solution that met the customer’s needs.

---

## **Overall**

This lab taught me how to look at a customer scenario, plan the right VPC design, and configure all the network parts that make it work. It also helped me practice explaining my work clearly, which is an important skill for cloud architecture, troubleshooting, and working with clients in AWS environments.

# Lab complete 🎓
## SECOND LAB: Build Your VPC and Launch a Web Server
Objectives After completing this lab, you should be able to:

- Create a virtual private cloud (VPC)
- Create subnets
- Configure a security group
- Launch an Amazon Elastic Compute Cloud (Amazon EC2) instance into a VPC

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

## Task 1: Create your VPC
- search for VPC
- Create VPC
- View VPC

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)


## Task 2: Create additional subnets
- choose Subnets
- choose Create subnet
- choose Create subnet

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

## Task 3: Associate the subnets and add routes
- choose Route Tables
- Choose Public Route Table
- Private Route Table
- Save associations

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

## Task 4: Create a VPC security group
- choose Security Groups
- Add rule
- Create security group.

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)


## Task 5: Launch a web server instance
- choose EC2
- choose Instances
- Launch instances
- Choose Launch instance.

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

![diagram](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)



=======
![AWS](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/networkingImages/awsCloud.PNG?raw=true)
>>>>>>> 4dd5934399f152cd42b38b3db45f69292a7f93a0
