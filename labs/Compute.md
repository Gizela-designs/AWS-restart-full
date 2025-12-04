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

![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/siteNotReached.PNG?raw=true)
![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/HelloServer.PNG?raw=true)

## TASK 4 :
## RESIZE YOUR INSTANCE

- Navigate to instance and select the web server you created
- Select instance state > Stop instance
- Instance must display stopped
- Change the instance to t3.small under Actions tab
- Resize volume under actions to 10 The desired outcome must display the new changes
  
![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/ec2(1).PNG?raw=true)

## TASK 5:
## TEST TERMINATION PROCESS

- Navigate to instance, and then select the web server you just created

- Under instance menu select the termination delete tab

- Bescause he it did not work, go to actions > select instance setting > change protection then uncheck ENABLE

- Go to actions again instance state > terminate instance
  
![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/ec2(2).PNG?raw=true)
![logo](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/computeImages/ec2(3).PNG?raw=true)

Here’s a fuller rewrite of your reflection:

# WHAT I LEARNED

I set up a web server using AWS by launching an EC2 instance and enabling termination protection to prevent accidental deletion
I monitored the performance of my server to ensure everything was functioning properly
I adjusted the security settings to allow web access so visitors could access my website via HTTP.
I learned how to scale my server, adjusting its power as needed based on my requirements.
I tested the termination protection by attempting to delete the server to confirm the safety feature worked as intended
Finally, I correctly shut down and removed the instance once I was done.

# SECOND LAB: AWS Lambda Exercise (Challenge) 177
Objectives After completing this lab, you will be able to do the following:

- Create a Lambda function to count the number of words in a text file.

- Configure an Amazon Simple Storage Service (Amazon S3) bucket to invoke a Lambda function when a text file is uploaded to the S3 bucket.

- Create an Amazon Simple Notification Service (Amazon SNS) topic to report the word count in an email

## challenge
- Create a Lambda function to count the number of words in a text file. The general steps are as follows:

- Use the AWS Management Console to develop a Lambda function in Python and create the function's required resources.

- Report the word count in an email by using an SNS topic. Optionally, also send the result in an SMS (text) message.

- Format the response message as follows:

- The word count in the file is nnn.

- Replace with the name of the file.

- Enter the following text as the email subject: Word Count Result

- Automatically invoke the function when the text file is uploaded to an S3 bucket.

- Test the function by uploading a few sample text files with different word counts to the S3 bucket.

- Forward the email that one of your tests produces and a screenshot of your Lambda function to your instructor.

# WHAT I LEARNED

- I created a Lambda function that counts the number of words in a text file, showing how AWS can run code automatically without needing a server
- I configured an S3 bucket so that whenever a text file is uploaded, it automatically invokes the Lambda function to process the file
- I set up an Amazon SNS topic to send an email notification with the word count, making it easy to get automated results.

# Lab Complete 🎓
