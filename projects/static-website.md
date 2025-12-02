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

# **Implementation Journey**

## **Phase One: Foundation and Provisioning**

**S3 Bucket Creation**
The initial task is the creation of the S3 bucket in the United States East region in Northern Virginia to ensure optimal integration with CloudFront.

**Configuration** | **Value** | **Reasoning**
**Bucket Name** | ember co | Clear brand identity and full compatibility with domain naming standards
**Region** | us east one | Provides the lowest latency for CloudFront with extensive global edge coverage
**Static Hosting** | Enabled | Allows the bucket to serve index html as the default document
**Versioning** | Enabled | Supports safe rollbacks and strengthens production stability

**Key Decision:**
Files are organized into clear and functional folders such as Images CSS and JS to support strong maintainability and reflect the structure of a professional production environment.

# Asset Upload Strategy


## Successfully uploaded 71 assets totaling 34MB:

- 45 high-resolution menu images
- 12 CSS files (including responsive frameworks)
- 8 JavaScript files (booking logic, animations)
- 6 HTML pages (homepage, menu, booking, about, contact, confirmation)
**Upload approach:** Used AWS CLI for batch operations rather than console clicking—faster, repeatable, scriptable.

## **Phase Two: Development Environment Setup**

**Initial Public Access Policy**
For accelerated development, a temporary bucket policy was configured to allow public read access. This approach enabled quick validation of assets and streamlined early testing.

**This was temporary**. Production required a more secure approach.

## Static Website Hosting Configuration

Activated static website hosting with proper error handling:

**Testing checkpoint:** Verified all pages loaded correctly, CSS/JS files resolved, images displayed without 403 errors.

## Phase 3: CloudFront Distribution & CDN

**Distribution Creation**

The true strength of the architecture is delivered through CloudFront. I created a distribution that pulls content directly from the S3 website endpoint.


| Setting | Configuration | Impact |
|-----------|------------|--------------|
| Origin Domain | ember-co.s3-website-us-east-1.amazonaws.com  | Website endpoint (not bucket endpoint) for proper routing    |
| Distribution Domain | dbmubhcukpnv9.cloudfront.net  | Auto-generated global CDN endpoint    |
| Price Class | All Edge Locations | Maximum global reach    |
| Default Root Object | index.html | Handles root URL requests    |
| Viewer Protocol | Redirect HTTP to HTTPS | Security best practice    |

## Phase 4: Production Security Hardening

**CloudFront-Only Access Policy**

Here's where architecture gets serious. Instead of leaving S3 public, I amended the bucket policy to only allow access from CloudFront:

**Why This Matters**
This distinction separates a casual hobby setup from a true enterprise-grade architecture. The S3 bucket is now fully secured with no direct public access and all traffic flowing exclusively through CloudFront. This design prevents several critical risks:

**• Bypassing the content delivery network, which can lead to unnecessary cost increases**
**• Distributed denial of service attacks targeting the S3 endpoint directly**
**• Attempts to access content without proper authorization controls**
**• Unauthorized consumption of bandwidth and other resources**

## Security Benefits:

-  AWS Shield Standard protection automatically enabled
-  CloudFront access logs for security auditing
-  Geographic restrictions available if needed
-  Custom SSL/TLS certificates supported
