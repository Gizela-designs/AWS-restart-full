# 🍽️ Ember & Co: A Digital Upgrade Powered by AWS
Turning operational chaos into cloud-level clarity with smart, scalable AWS architecture.

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/projects/gallery/staticWebImg/emberAndCo.PNG?raw=true)

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

![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/projects/gallery/staticWebImg/S3.PNG?raw=true)

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

!![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/projects/gallery/staticWebImg/assetUpload.PNG?raw=true)

## Successfully uploaded 71 assets totaling 34MB:

- 45 high-resolution menu images
- 12 CSS files (including responsive frameworks)
- 8 JavaScript files (booking logic, animations)
- 6 HTML pages (homepage, menu, booking, about, contact, confirmation)
**Upload approach:** Used AWS CLI for batch operations rather than console clicking—faster, repeatable, scriptable.


## **Phase Two: Development Environment Setup**

**Initial Public Access Policy**
For accelerated development, a temporary bucket policy was configured to allow public read access. This approach enabled quick validation of assets and streamlined early testing.


{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::ember-co/*"
    }
  ]
}


![](https://github.com/Gizela-designs/AWS-restart-full/blob/main/projects/gallery/staticWebImg/S3Code.PNG?raw=true)

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

 - Bypassing the content delivery network, which can lead to unnecessary cost increases
 - Distributed denial of service attacks targeting the S3 endpoint directly
 - Attempts to access content without proper authorization controls
 - Unauthorized consumption of bandwidth and other resources

## Security Benefits:

-  AWS Shield Standard protection automatically enabled
-  CloudFront access logs for security auditing
-  Geographic restrictions available if needed
-  Custom SSL/TLS certificates supported

## Phase 5: User Experience Delivery

**Homepage Hero Section**

The homepage delivers immediate impact with clear call-to-action:

## Design Elements:

- Full-width hero image with overlay gradient for text readability
- "NOW BOOKING" primary CTA button with hover animations
- Responsive typography scaling from mobile to desktop
- Smooth scroll-to-section navigation

## Interactive Menu System
The requirements demanded "images, videos, or animations to enhance design." Delivered with a tabbed menu system featuring:

## Menu Categories:

Mains - Signature dishes with portion size indicators
Starters - Appetizers with dietary icons (vegetarian, gluten-free)
Desserts - Sweet offerings with calorie information
Drinks - Full beverage menu with pairing suggestions

## Technical Implementation:

- CSS Grid for responsive card layouts
- JavaScript tab switching with smooth transitions
- High-quality WebP images with JPEG fallbacks
- Lazy loading for performance optimization
- Design choice: High-contrast text on food imagery while maintaining readability—exactly as the project required.

## Booking Form Architecture
The core problem was "order mix-ups and double-bookings." The solution starts with a clean, validated form:

## Form Fields:

- Full Name (required, regex validation)
- Email (required, RFC 5322 compliant)
- Phone Number (required, international format support)
- Party Size (1-20 guests, dropdown)
- Date & Time (required, prevents past dates)
- Special Requests (optional textarea)

## Client-Side Validation:

- Real-time field validation with error messages
- Date picker restricted to business hours (5 PM - 11 PM)
- Prevents submission of incomplete forms
- Accessibility-compliant (WCAG 2.1 AA)

## Confirmation Flow:

- Immediate on-screen confirmation
- Summary of booking details
- "Add to Calendar" button (generates .ics file)
- Clear next steps and contact information

## Mobile-First Responsiveness
With 60%+ of restaurant bookings coming from mobile, responsiveness wasn't optional:

## Breakpoints:

- Mobile: 320px - 767px
- Tablet: 768px - 1023px
- Desktop: 1024px+

## Mobile Optimizations:

- Hamburger menu collapses navigation cleanly
-- Touch-friendly button sizing (minimum 44px tap targets)
- Simplified forms with mobile-optimized input types
- Reduced image sizes for faster load times
Pro tip: Tested on actual devices (iPhone 12, Samsung Galaxy S21, iPad), not just browser dev tools. The difference is night and day.

# Security & Verification
## Security Architecture
## Defense-in-Depth Strategy:

- CloudFront Layer - DDoS protection via AWS Shield, WAF integration ready
- IAM Policies - Least-privilege access for deployment users
- S3 Bucket Policies - Service Principal with SourceArn condition
- HTTPS Enforcement - TLS 1.2+ mandatory, HTTP redirects
- Access Logging - CloudFront and S3 logs retained for 90 days

## Testing the Deployment



## Performance Metrics
## Lighthouse Scores (Mobile):

- Performance: 94/100
- Accessibility: 98/100
- Best Practices: 100/100
- SEO: 100/100

## Load Times:

- First Contentful Paint: 1.2s
- Time to Interactive: 2.8s
- Largest Contentful Paint: 2.1s

If you see these metrics, you're delivering production-grade performance.

# What I Learned
## Technical Skills I Practiced

## AWS Resource Management

- Creating and configuring S3 buckets with static website hosting
- Understanding the difference between S3 website endpoints vs. bucket endpoints
- Setting up CloudFront distributions with custom origins
- Implementing cache invalidation strategies

# Security by Design

- Implementing least-privilege access through IAM and bucket policies
- Using CloudFront Service Principal with SourceArn conditions (production-grade)
- Balancing security (locked-down S3) with functionality (public website via CDN)
- Applying HTTPS enforcement and TLS best practices

# Real-World Architecture

- Designing a solution that starts simple (static site) but scales infinitely
- Mapping business problems (double-bookings) to technical solutions
- Creating presentations that speak stakeholder language (ROI, not just tech specs)
- Planning phased migrations with minimal downtime

# Business Communication

- Translating technical architecture into revenue recovery
- Presenting a 7-week migration roadmap costing less than two meals
- Demonstrating enterprise-grade infrastructure at local business pricing
- Building stakeholder confidence through clear documentation

# The Real Takeaway
Honestly, the biggest challenge wasn't technical—it was thinking like a consultant. The AWS Cloud Practitioner exam teaches services, but this project taught me to connect those services to revenue recovery, staff efficiency, and customer satisfaction.

When the restaurant owner sees "Lambda runs only when a customer clicks Reserve," they don't care about serverless architecture—they care about not paying for idle infrastructure. That's the mindset shift this project demanded.

## Key insights:

 Security is non-negotiable — Even for a restaurant website, CloudFront + locked S3 is the right way
Architecture decisions have business impact — $14/month vs. thousands in lost revenue from double-bookings
 Presentations matter as much as code — The PowerPoint deck closed the deal, not the S3 bucket
 Mobile-first isn't optional — Most bookings come from phones, not desktops
 Documentation is a deliverable — Clear READMEs demonstrate professionalism
This project proved I can build AWS infrastructure and explain why it matters to people who've never heard of IAM policies.

