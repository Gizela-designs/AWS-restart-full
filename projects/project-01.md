# 🍽️ Ember & Co: A Digital Upgrade Powered by AWS
Turning operational chaos into cloud-level clarity with smart, scalable AWS architecture.

# 📋 What's Inside
- What I Built Here
- Architecture Overview
- Implementation Journey
- Security & Verification
- What I Learned


## What I Built Here

This project was designed to solve a real operational problem for Ember & Co, a well-known restaurant in Melville that serves more than 100 customers a day with a 25% profit margin. Their booking process was completely manual, which led to double-bookings, lost reservations, and unnecessary pressure on staff.

As the business grew, the old system couldn’t keep up. Processes that worked at a small scale simply collapsed under higher demand. My goal was to build a cloud solution that matched their pace and removed the bottlenecks that were slowing them down.

**To fix this, I built a complete cloud-based experience:**

- I created a fully functional static website with a clean booking interface.

- I designed a serverless backend architecture that can support future dynamic features like automated confirmations or customer analytics.

- I secured the AWS environment using correct IAM roles and access policies.

- I translated the technical work into business value so stakeholders could understand the return on investment, not just the technical details.

Tech Stack: Amazon S3, CloudFront, Route 53, IAM, Business Strategy & Consulting

# Architecture Overview
## How It’s Built

The goal wasn’t to “just upload files to the cloud.” I built a serverless architecture that can grow as the business grows. What looks simple on the front end is supported by a reliable, scalable, enterprise-ready AWS infrastructure underneath.

# Key Pieces of the Architecture

The system is built from multiple AWS services working together, each handling a specific part of the solution.
The static content is stored in Amazon S3 and delivered through CloudFront, giving users a fast-loading menu and pages with extremely high durability. Route 53 handles the domain so the website loads with a professional, reliable DNS setup.

For future dynamic features, I architected a full serverless backend using API Gateway, Lambda, DynamoDB, and Simple Email Service. This forms the backbone of a zero-error booking engine that can scale without servers.

Security is enforced at every layer using IAM roles and strict bucket policies. Anyone can make resources public—what matters is securing them properly while still keeping the system usable. That part of the project required the most attention and precision.

# Infrastructure Design

The overall design follows AWS best practices and keeps development and production environments clearly separated. This prevents accidental changes and supports safer updates.

## Content Delivery:
CloudFront acts as the global CDN, caching the site at edge locations so pages load in under 100 milliseconds for most users.

## Storage:
S3 stores all the website files and uses versioning, which allows you to roll back instantly if something goes wrong.

## Security:
IAM and bucket policies apply a strict, zero-trust model, ensuring only the right services and users have access.

## DNS:
Route 53 manages the domain, giving the system reliable, enterprise-level name resolution.

## Monitoring:
CloudWatch tracks performance, logs activity, and helps detect errors or unusual behavior in real time.



