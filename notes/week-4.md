# Week 4
## Core Data Security Ideas

- Security in the cloud is all about protecting your data from every angle. One of the most important concepts is Defense in Depth. Instead of depending on a single security measure, you stack multiple layers of protection. Imagine locking your house with more than one lock. Even if someone picks the first one, they still have more obstacles to get past. In the same way, firewalls, identity controls, and encryption work together to keep your information safe.

- Another major idea is the Shared Responsibility Model. AWS and the customer work together to secure cloud environments. AWS takes care of all the physical components such as data centers, servers, and the underlying network that keeps everything running. Your job is to secure what you build on top of that. This includes your data, your applications, and deciding who gets access through AWS services.

- It is also important to understand your data. Not all information is equal. For example, customer payment information or health records must be handled more carefully than general logs or test files. Knowing which data is sensitive helps you apply the right level of protection.

- Encryption is a powerful tool that protects your data by turning it into unreadable text unless someone has the right key. Encrypting data at rest means securing the data stored on disks, such as in S3 or EBS volumes. Encrypting data in transit means protecting it while it travels over the internet. Whenever you see the padlock icon and the https prefix in your browser, you are using encrypted communication. Client side encryption takes place on your own computer before data is even uploaded to AWS.

- AWS provides tools such as Key Management Service, or KMS, which helps you create, store, and manage your encryption keys. Services like S3 and EBS also support automatic encryption so you do not need to handle everything manually.

## Controlling Access with IAM

Identity and Access Management, or IAM, is your main tool for defining who can do what inside your AWS account. A user represents an individual person with a username and password. Groups make it easier to manage multiple people at once by giving them shared permissions, such as a group for developers or administrators. Roles serve as temporary security passes that applications or services can use to access AWS without needing a long term user account. Policies describe exactly what actions are allowed or denied.

Several best practices are especially important.
The principle of least privilege means giving people only the access they truly need and nothing more. This reduces the risk of mistakes or misuse.
Using multi factor authentication adds a second step to the login process, usually a code sent to your phone, which dramatically increases security.
Where possible, use roles instead of long lasting access keys. Keys are often forgotten, leaked, or misused, while roles provide safer temporary access.

## Understanding Compliance

AWS supports many global standards that deal with safety, privacy, and regulation. Examples include PCI DSS for credit card information, HIPAA for healthcare, and GDPR for data protection in Europe. AWS Artifact is the centralized place where you can download compliance reports and certifications to show that AWS meets industry requirements. This can help organizations prove that they handle data responsibly.

## Tracking Activity with AWS CloudTrail

CloudTrail works like a security camera for your AWS account. It records every action taken by a user or service. If something goes wrong, you can look back to understand exactly who did what. This is incredibly helpful for security investigations, troubleshooting issues with applications, and meeting compliance requirements that require detailed logging.

## Monitoring EC2 with CloudWatch

CloudWatch helps you understand how healthy your EC2 instance is. It gathers information such as CPU usage, memory pressure, and network traffic. For example, if the CPU is constantly maxed out, you may need a larger instance. If network traffic spikes, you may be receiving more visitors or experiencing a security event. Monitoring these metrics helps you act before problems grow.

## Strengthening Network Security in Your VPC

- A VPC is your own private environment inside AWS, separated from everyone else. Security groups act like firewalls that protect individual EC2 instances. They decide what can enter and what can leave. Because they are stateful, if you allow incoming traffic, the return traffic is automatically allowed.

- Network ACLs protect entire subnets and give you another layer of control. They are stateless, which means you must set up both incoming and outgoing rules. This makes them more strict and useful for large scale filtering.

- Private subnets are ideal for resources that should never be accessed directly from the internet, such as databases. Keeping them isolated greatly reduces security risks.
VPC Flow Logs record all the information about traffic entering or leaving your network interfaces, making them extremely useful for analyzing unusual behavior or troubleshooting connectivity issues.

## Choosing the Right Numeric Data Types

When designing a database, choosing the right type of number is important for accuracy and performance.
Integers are perfect for whole numbers such as user IDs or counters.
Decimals are used when precision matters, like when working with money, because they prevent rounding errors.
Floating point numbers are used for scientific or statistical data where small rounding differences are acceptable.

A good rule is to choose the smallest data type that safely fits your needs. This keeps your database efficient and can improve performance.

## Personal Note

When I first learned about cloud security, it felt overwhelming because there were so many new tools, concepts, and responsibilities. What helped most was realizing that cloud security works just like real world security. If you lock your doors, verify who enters, keep valuable items protected, and monitor activity around your space, you are already following the same principles. AWS simply gives you digital tools to do all of that at scale. Understanding the shared responsibility model and seeing how encryption, IAM, and VPC security work together made everything click, and now cloud security feels far more manageable and logical.