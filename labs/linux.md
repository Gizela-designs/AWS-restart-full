# LINUX
I will share two from this topic that i found interesting. The first is the Bash Shell Scripting and the second is the Challenge we were given to yield a certain outcome.

#FIRST LAB: BASH SHELL SCRIPTING
Objectives In this lab, you will:

- Create a bash script that will automate the backup of a folder.

## TASK 1
Firstly i have to follow this instructions to connect using SSH:

- Select the Details drop-down menu above these instructions you are currently reading, and then select Show. A Credentials window will be presented.

- Select the Download PPK button and save the labsuser.ppk file. Typically your browser will save it to the Downloads directory.

- Make a note of the PublicIP address.

- Then exit the Details panel by selecting the X.

- Download PuTTY to SSH into the Amazon EC2 instance. If you do not have PuTTY installed on your computer, download it here.

- Open putty.exe

## TASK 2
Write a shell script

I need to create a Bash shell script that automatically backs up the CompanyA folder by compressing it into an archive file. I'll name the archive using today's date followed by "-backup-companyA.tar.gz"

**STEPS TAKEN**

-Validate that im in the home folder by typing pwd

outcome is a s follows :



create a generic shell script called backup.sh



change the file privileges to make backup.sh



use my preferred text editor to open the backup.sh file for editing

To activate insert mode

create a variable for the current date



create a variable for the backup file for the day

saved my script and exit from the editor



run backup.sh



verify that the archive is created in the backups folder

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/logInUser.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/backUp.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/binBash.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/binBasg2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/endBackup.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/ec2User.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/linuxImages/ec2User2.PNG?raw=true)

# WHAT I LEARNED

- I wrote a bash script that automatically backs up a folder, so I don't have to manually copy files every time

# Lab Complete 🎓





