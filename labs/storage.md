# STORAGE
Under storage we have a few labs, i will share 2 labs i found intriguing

# FIRST LAB

Objectives

- By the end of this lab, you will be able to do the following:
- Create an EBS volume.
- Attach and mount an EBS volume to an EC2 instance.
- Create a snapshot of an EBS volume.
- Create an EBS volume from a snapshot.

I worked through a hands-on lab with Amazon EBS volumes, learning how to create, attach, snapshot, and restore storage on AWS. Here's what I did.

# Task 1
I started by navigating to the EC2 service in my AWS Console. I clicked "Create volume" and added a tag to help me identify it later—I set the Key as "Name" and the Value as "My Volume." Then I created the volume.

# Task 2
Once my volume was ready, I selected "My Volume" and clicked "Attach volume." I chose my Lab instance from the dropdown and confirmed the attachment.

# Task 3
I connected to my EC2 instance using SSH so I could work directly on the Linux system.

# Task 4 

- Viewed the existing storage to see what was available
- Created an ext3 file system on my new volume
- Created a directory to serve as the mount point
- Mounted the new volume to that directory
- Checked the configuration file to verify everything
- Viewed the available storage again to confirm the mount was successful
- Created a test file and added some text to it on the mounted volume
- Verified that the text was properly written to my volume

# Task 5
I went back to the Volumes section and selected "My Volume." Then I deleted the file I had created on the volume and verified it was actually gone.

# Task 6

- Task 6.1: Creating a Volume from the Snapshot I selected "My Snapshot" and created a new volume from it. I tagged this one with the Key "Name" and Value "Restored Volume," then created the volume and navigated to the Volumes section.
- Task 6.2: Attaching the Restored Volume to My EC2 Instance I selected "Restored Volume," clicked "Attach volume," chose my Lab instance, and attached it.
- Task 6.3: Mounting the Restored Volume Finally, I created a new directory for mounting the restored volume, mounted it, and verified that everything was working correctly.

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/amazonEBS.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/createVolume.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/createdVolume.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/ec2Terminal1.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/ec2Terminal2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/ec2Terminal3.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/mySnapshot.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/snapshotCreated.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/attachVolume.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/volumes2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/ec2Terminal4.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/storageImages/ec2Terminal5.PNG?raw=true)


# WHAT I LEARNED

- I made an EBS volume, which is like adding a new hard drive to my server in the cloud.
- I attached the EBS volume to an EC2 instance and mounted it so I could actually use it to store files.
- I created a snapshot of my EBS volume, which is basically a complete backup of all the data at that moment
- I learned how to create a brand new EBS volume from that snapshot, which is useful for copying data or recovering from problems

# Lab complete 🎓
# SECOND LAB: Challenge Lab: Amazon S3
I completed a hands-on challenge working with the AWS Command Line Interface (CLI) and Amazon S3. Here's how I tackled it.

- Task 1: Connecting to the CLI Host Instance I started by connecting to my EC2 instance via SSH. This gave me direct access to the command line where I could start working with AWS services.
- Task 2: Configuring the AWS CLI Once connected, I used the SSH client to set up and configure the AWS CLI on my EC2 instance. This step was crucial because it allowed me to interact with AWS services directly from the command line.
- Task 3: Finishing the Challenge This is where I put everything together and completed the actual challenge.
- Creating the Bucket I used the AWS CLI to create a new S3 bucket. This was my first time creating cloud storage from the command line instead of clicking through the console.
- Uploading an Object
- Next, I uploaded a file (an object) into my newly created S3 bucket using CLI commands.
- Listing the Bucket Contents I ran a command to list all the contents of my S3 bucket, verifying that my uploaded file was actually there. Seeing the output in the terminal confirmed everything worked correctly.
- Accessing the Object via Web Browser Finally, I accessed my uploaded object using a web browser to prove that it was publicly accessible and properly stored in S3.

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/storageImages/ec2Challenge.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/storageImages/AmazonS3.PNG?raw=true)

# WHAT I LEARNED

- I set up an S3 bucket, which works like creating a dedicated folder in the cloud for storing data.
- I uploaded an object into the bucket so I could store and manage data directly in S3.
- I learned how to open the object in a web browser, showing how S3 can be used to make files publicly accessible when needed
- I used the AWS CLI to list everything inside the S3 bucket, which is helpful for managing and checking files through the command line

# Lab complete 🎓


