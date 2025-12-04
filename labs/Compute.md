# Setting up and launching an EC2 instance

## Topics covered
1. Launch a web server with termination protection enabled

2. Monitor Your EC2 instance

3. Modify the security group that your web server is using to allow HTTP access

4. Resize your Amazon EC2 instance to scale

5. Test termination protection

6. Terminate your EC2 instance

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/images/ec2(1).PNG?raw=true)


## TASK 1 :
## LAUNCH EC2 INSTANCE

- Name the instance
- Choose an Amazon machine image
- Choose an instance type
- Configure a key pair
- Configure the network settings
- Add storage
- Configure advanced network settings
- Then finally launch the instance

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/instance.PNG?raw=true)

## TASK 2 :
## MONITOR THE INSTANCE

- Monitor and troubleshoot to get the this outcome THIS IS THE OUTCOME

![logo]()

## TASK 3 :
## UPDATE SECURITY RULES AND ACCESS THE WEB SERVER

- Go to network & security
- The select security groups
- select inbound rules
- Edit the rules with the following : - Type: HTTP Source: Anywhere-IPv4
- Save the rules and reload web server to see the desired outcome. THIS IS THE OUTCOME


![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/ChoosinganInstancetype.PNG?raw=true)

## Configuring the network settings
The VPC indicates which virtual private cloud (VPC) you want to launch the instance into. You can have multiple VPCs, including different ones for development, testing, and production. In the Network settings pane, choose Edit For VPC - required, select Lab VPC. Still in the Network settings pane, configure the Security Group as follows: Security group name - required: Web Server security group Description: Security group for my web server A security group acts as a virtual firewall that controls the traffic for one or more instances. When you launch an instance, you associate one or more security groups with the instance. You add rules to each security group that allow traffic to or from its associated instances. You can modify the rules for a security group at any time; the new rules are automatically applied to all instances that are associated with the security group. Under Inbound security groups rules select the Remove In this lab, you will not log into your instance using SSH. Removing SSH access will improve the security of the instance.

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/NetworkConfiguration.PNG?raw=true)

## Adding storage
Amazon EC2 stores data on a network-attached virtual disk called Amazon Elastic Block Store (Amazon EBS). You launch the EC2 instance using a default 8 GiB disk volume. This is your root volume (also known as a boot volume). EC2

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/Configurestorageneeded.PNG?raw=true)

## Configuring advanced details
Expand the Advanced details pane. Select the dropdown for Termination protection, then choose Enable. When you launch an instance in Amazon EC2, you have the option of passing user data to the instance. These commands can be used to perform common automated configuration tasks and even run scripts after the instance starts. Copy the following commands, and paste them into the User data text box.

#!/bin/bash yum -y install httpd systemctl enable httpd systemctl start httpd echo '

![logo](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

# Hello From Your Web Server!
' > /var/www/html/index.html
The script does the following: Install an Apache web server (httpd) Configure the web server to automatically start on boot Activate the Web server Create a simple web page

![logo](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

## Launching an EC2 instance
Now that you have configured your EC2 instance settings, it is time to launch your instance. In the right pane, choose Launch instance Choose View all instances The instance appears in a Pending state, which means it is being launched. It then changes to Running, which indicates that the instance has started booting. There will be a short time before you can access the instance. The instance receives a public DNS name that you can use to contact the instance from the Internet. Select the box next to your Web Server. The Details tab displays detailed information about your instance. To view more information in the Details tab, drag the window divider upward. Review the information displayed in the Details, Security and Networking tabs. Wait for your instance to display the following: Note: Refresh if needed. Instance State: Running Status Checks: 2/2 checks passed

![logo](810%20×%20525%20pixels%20—%2037.83%30KB%20labs/networkingImages/awsCloud.PNG)

## Monitor Your Instance
Monitoring is an important part of maintaining the reliability, availability, and performance of your Amazon Elastic Compute Cloud (Amazon EC2) instances and your AWS solutions. Select the instance by checking the box next to the instance and navigate to the bottom of the screen to the Status checks tab. With instance status monitoring, you can quickly determine whether Amazon EC2 has detected any problems that might prevent your instances from running applications. Amazon EC2 performs automated checks on every running EC2 instance to identify hardware and software issues. Notice that both the System reachability and Instance reachability checks have passed. Select the Monitoring tab. This tab displays Amazon CloudWatch metrics for your instance. Currently, there are not many metrics to display because the instance was recently launched. You can choose a graph to see an expanded view. Amazon EC2 sends metrics to Amazon CloudWatch for your EC2 instances. Basic (five-minute) monitoring is enabled by default. You can enable detailed (one-minute) monitoring. In the Actions menu, select Monitor and troubleshoot Get Instance Screenshot. This shows you what your Amazon EC2 instance console would look like if a screen were attached to it.

![logo](C:\Users\admin\Pictures\Capture.JPG)

## Update Your Security Group and Access the Web Server
When you launched the EC2 instance, you provided a script that installed a web server and created a simple web page. In this task, you will access content from the web server. Select the instance by checking the box and select the Details tab. Copy the Public IPv4 address of your instance to your clipboard. Open a new tab in your web browser, paste the IP address you just copied, then press Enter. Question: Are you able to access your web server? Why not? You are not currently able to access your web server because the security group is not permitting inbound traffic on port 80, which is used for HTTP web requests. This is a demonstration of using a security group as a firewall to restrict the network traffic that is allowed in and out of an instance. To correct this, you will now update the security group to permit web traffic on port 80. Keep the browser tab open, but return to the EC2 Management Console tab. In the left navigation pane, select Security Groups located under Network & Security. Select Web Server security group. Select the Inbound rules tab. The security group currently has no rules.

Select Edit inbound rules then select Add rule and configure the rule with the following settings: Type: HTTP Source: Anywhere-IPv4 Select Save rules Return to the web server tab that you previously opened and refresh the page. You should see the message Hello From Your Web Server!
