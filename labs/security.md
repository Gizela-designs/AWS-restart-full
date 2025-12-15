# SECURITY
Under Security, we had a few labs to do. I will showcase 2 labs from this topic

# FIRST LAB: SECURITY-HARDENING
I worked through a hands-on lab with AWS Systems Manager Patch Manager, learning how to patch Linux and Windows instances, create custom baselines, and verify compliance. Here's what I did.

# Task 1: Patching Linux Instances with Default Baseline
- I navigated to Systems Manager and selected Fleet Manager under Node Management. I checked the Linux-1 instance details, then went to Patch Manager and chose "Patch now." I configured the patching operation to scan and install with reboot if needed, targeting instances with the tag "Patch Group: LinuxProd." This patched my Linux instances using the default AWS baseline.

# Task 2: Creating a Custom Patch Baseline for Windows
- In Patch Manager, I selected the "Patch baselines" tab and clicked "Create patch baseline." I named it "WindowsServerSecurityUpdates," set the operating system to Windows, and left it as a non-default baseline. Then I selected my new baseline, chose "Modify patch groups" from the Actions menu, and added "WindowsProd" as the patch group.

# Task 3: Tagging and Patching Windows Instances
- I went to EC2 and tagged all three Windows instances (Windows-1, Windows-2, and Windows-3) with Key: "Patch Group" and Value: "WindowsProd." Then I returned to Patch Manager, clicked "Patch now," and configured it to scan and install patches on instances with the "Patch Group: WindowsProd" tag.

# Task 4: Verifying Patch Compliance
- I checked the Compliance reporting tab in Patch Manager to verify that all my Linux and Windows instances were properly patched and compliant.

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/securityHardening1.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/securityHardening2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/securityHardening3.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/Patch1.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/Patch2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/modifyPatch.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/modifyPatch2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/tag1.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/tag2.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/patchCompliance.PNG?raw=true)
![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/labs/gallery/securityImages/patchCompliance2.PNG?raw=true)

# WHAT I LEARNED

- I learned how to use AWS Systems Manager to automatically patch Linux servers using Amazon's default security updates
- I figured out how to make a custom patch baseline, which lets me decide exactly which updates get installed and when
- I learned to use patch groups to manage Windows servers separately, so different groups can have different patching schedules and rules.
- I verified patch compliance to see which servers were properly updated and which ones might have missed patches

# Lab complete 🎓
# SECOND LAB: Introduction to AWS Identity and Access Management (IAM)
I worked through a hands-on lab with AWS Identity and Access Management (IAM), learning how to create password policies, manage user groups, and test user permissions. Here's what I did.

# Task 1: Creating a Custom Password Policy
I navigated to IAM and selected "Account settings." I clicked "Change password policy" and configured:

- Minimum password length: 10 characters
- Selected all checkboxes except "Password expiration requires administrator reset"
- Password expiration: 90 days
- Prevent password reuse: 5 passwords

# Task 2: Exploring Users and User Groups
I explored the existing IAM setup by viewing user-1's groups and security credentials. Then I examined three user groups and their permission policies:

- EC2-Support: Read-only EC2 access
- EC2-Admin: Full EC2 administrative rights

# Task 3: Adding Users to User Groups
I assigned users to their groups:

- user-1 → S3-Support group
- user-2 → EC2-Support group
- user-3 → EC2-Admin group

# Task 4: Testing User Permissions
I copied the IAM Sign-in URL and tested each user in private windows:

- user-1: Successfully accessed S3 but couldn't access EC2.
- user-2: Accessed EC2 and viewed instances but couldn't stop them (read-only). Had no S3 access.
- user-3: Had full EC2 admin access and successfully stopped an instance.

# What I learnt
I learned how to control who can access what in AWS, how to organize users efficiently, and how policies actually affect what people can do once they log in.Retry

# Lab complete 🎓

