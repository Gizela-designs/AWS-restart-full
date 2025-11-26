# Week 7 Notes
## AWS Well-Architected Framework

The AWS Well-Architected Framework is a guide that teaches you how to build systems in the cloud that are secure, fast, reliable, and cost-efficient. Think of it as a checklist of best practices for designing anything from a small project to a large enterprise system. The framework is built around six major pillars that help you evaluate your architecture and spot areas for improvement. When you follow the pillars, you end up with workloads that scale smoothly, recover from failures, and avoid unnecessary spending.

## **The Six Well-Architected Pillars**

## **Operational Excellence**
This pillar focuses on how you run your systems day-to-day. Automating everything is the key idea. Automate deployments, automate monitoring, and automate rollbacks when something goes wrong. Use version control for all changes, and aim for small updates that can easily be reversed. Observability matters too, so make sure you can see exactly what your system is doing at any given moment.

## **Security**
Security is all about protecting your data and your systems. Follow the principle of least privilege so every user and service only gets the access it truly needs. Use multi-factor authentication and encryption everywhere. Enable logging so you can see who did what. Automating your security checks helps catch issues early before they turn into real problems.

## **Reliability**
A reliable system keeps running even when something fails. You should always assume failures will happen and design for them. Use multiple Availability Zones, automatic scaling, health checks, and regular backups. Test your recovery process instead of waiting for an emergency to find out something doesn’t work.

## **Performance Efficiency**
This pillar is all about using the right tools for the job. Choose the compute and storage options that best match your workload. Use managed services to reduce overhead. Scale horizontally so you can handle growing traffic smoothly. The idea is to avoid bottlenecks and ensure your application runs efficiently at all times.

## **Cost Optimization**
AWS gives you many ways to control costs, but you need to be intentional. Only pay for the resources you actually use. Monitor your spending and set budgets or alarms. Right-size your compute and storage, and use reserved instances or savings plans when you know you will be running things long-term. The more you understand your workload, the more you can save.

## **Sustainability**
This pillar encourages designing cloud systems that use energy efficiently. Choose instance types that maximize performance per watt and avoid unnecessary compute waste. Serverless architectures help reduce environmental impact because they only run when needed. Optimizing your workloads not only saves money but also helps reduce energy usage overall.

---

# **AWS CLI**

The AWS Command Line Interface is a tool that lets you interact with AWS services through commands instead of clicking around in the console. It is especially useful for automation, scripting, and CI/CD pipelines. You can configure it with your credentials using the command `aws configure`. From there you can list S3 buckets, view EC2 instances, create resources, or manage your environment from a terminal window. The CLI uses IAM permissions in the background, which means it will only let you do things your user or role has permission to do.

---

# **AWS IAM**

- IAM, short for Identity and Access Management, is the service that controls who can access your AWS resources and what actions they are allowed to take. It is built around a few key parts. Users are individual logins. Groups collect users together so they can share permissions. Roles are temporary access identities that AWS services or trusted users can assume. Policies are documents written in JSON that describe exactly what actions are allowed or denied.

- Some important best practices include always using least privilege, enabling multi-factor authentication for every user, avoiding the root account unless absolutely necessary, and regularly rotating access keys. A well-designed IAM setup is one of the foundations of a secure cloud environment.

---

# **Operations on AWS**

- Operations in AWS focus on managing, monitoring, and maintaining the workloads you build. Several AWS services play key roles here. CloudWatch collects logs, metrics, and alarms so you can keep an eye on your application's health. CloudTrail records all API activity so you can see who made changes or accessed resources. AWS Config tracks your resource configurations and helps you stay compliant. Systems Manager helps you automate patching, gather system inventory, and manage servers at scale.

- Good cloud operations involve deploying updates safely, monitoring performance and costs, securing and backing up your resources, and regularly testing your disaster recovery plan. When you combine these habits, you keep your environment efficient, secure, and ready for anything.

