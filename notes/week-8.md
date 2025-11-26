# Week 8 Notes
## Amazon EC2 Scaling

Scaling in the cloud is similar to adjusting the number of workers in a restaurant when it gets busy or quiet. AWS gives you two main ways to scale your EC2 instances.

## **Vertical Scaling (Scaling Up or Down)**
Vertical scaling means increasing or decreasing the size of your server. It is like replacing a normal computer with a more powerful one when you need extra performance. This approach is simple and works well for predictable workloads, but it usually requires stopping the instance while it changes. An example would be upgrading from a t2.micro instance to a t2.large.

## **Horizontal Scaling (Scaling Out or In)**
Horizontal scaling adds or removes servers instead of resizing a single one. You can think of this as bringing in more workers during a rush. This is the method most cloud applications use because it handles unpredictable traffic more effectively. AWS makes this easier through Auto Scaling Groups, which adjust the number of instances automatically.

## **Auto Scaling**
With Auto Scaling, AWS watches your system and launches or shuts down instances based on rules you choose. For example, you can set a rule that adds another server whenever CPU usage goes above eighty percent. This approach keeps your application responsive and saves money because you only pay for the resources you truly need.

---

## **Amazon Elastic Beanstalk**

Elastic Beanstalk is like having an assistant who takes care of your entire infrastructure setup for you. You simply upload your application code, and Beanstalk creates everything behind the scenes, from EC2 instances and load balancers to networking and monitoring. It is designed so developers can focus on writing code instead of configuring servers.

## **How the Beanstalk Workflow Looks**
- You start by uploading your application in whatever language you prefer, such as Python, Java, or Node. Beanstalk automatically builds the environment, including the servers, the connections, and the monitoring tools. Once the environment is ready, your application becomes available for users. When you want to update your app, you upload new code and Beanstalk handles the deployment process safely. It also monitors your environment and can scale automatically as your traffic changes.

- This service is especially helpful for new developers who want quicker deployments without giving up the option to customize configurations later.

---

## **Amazon API Gateway**

- API Gateway acts like a receptionist for your backend applications. It handles every incoming request, decides whether the request is valid, and then forwards it to the correct backend service such as Lambda, EC2, or a container. After your backend processes the request, the response travels back to the client through API Gateway.

- API Gateway includes important features like authentication and security controls, request throttling to prevent overload, and detailed monitoring for every API call. It works extremely well with Lambda, making it a core piece of many serverless applications.

---

## **Containers on AWS**

Containers are small, lightweight packages that include your application and everything it needs to run. They ensure the app behaves the same everywhere, whether it is running on your laptop or in the AWS environment. They are faster and more efficient than traditional virtual machines.

## **AWS offers several ways to run containers:**
- Amazon ECS manages containers the AWS-native way. You tell ECS what to run and it orchestrates all the tasks for you.
- Amazon EKS is AWS’s managed Kubernetes service, perfect for teams already using Kubernetes or needing advanced orchestration features.
- AWS Fargate removes servers entirely and lets you run containers without managing any underlying infrastructure. You only pay for the resources your containers actually use.

- Containers are especially useful for microservices, testing environments, and applications that need consistent behavior across development and production.

---

## **Elastic Load Balancing**

A load balancer is like a traffic controller standing at a busy intersection. It distributes incoming requests across multiple servers so that no single machine becomes overloaded. If a server fails, the load balancer automatically sends traffic to the healthy ones, which improves reliability and availability.

## **Types of load balancers include:**
- Application Load Balancers, which are ideal for web apps and can route requests based on the URL path.
- Network Load Balancers, which handle enormous numbers of requests with extremely high speed at the network level.
- Classic Load Balancers, which are older versions still supported but not recommended for new applications.

The overall process is simple. A user sends a request, the load balancer checks which servers are healthy, and the traffic is distributed evenly.

---

## **CloudFront**

- CloudFront is AWS’s content delivery network. It stores cached copies of your files at edge locations around the world so users access content from the closest location to them. This results in faster load times and reduced pressure on your origin servers.

- When a user requests something, CloudFront checks if it already has the file. If it does, the file loads almost instantly. If not, CloudFront retrieves the file from your origin server, delivers it to the user, and caches it for future requests.

- CloudFront is commonly used for websites, video streaming, image delivery, and even APIs. It also includes security features like built-in DDoS protection.

---

## **Route 53**

- Route 53 is AWS’s domain name system service. Its job is to take a human-friendly domain like [www.example.com](http://www.example.com) and map it to the IP address of the server where your application lives. It works like the internet’s phone book.

- Route 53 can register domain names, route traffic to your resources, and check the health of your servers. It supports many routing methods, including simple routing, failover routing, weighted routing, location-based routing, and latency-based routing. All of this ensures that users reach your application in the fastest and most reliable way possible.

---

## **How These Services Work Together**

- AWS services often combine to create powerful architectures. For example, you might use Route 53 to direct traffic to CloudFront, which delivers a static website from S3. Or you might build a web application where Route 53 sends requests to a load balancer, the load balancer distributes the traffic to Auto Scaling EC2 instances, and each instance runs code deployed by Elastic Beanstalk. For serverless microservices, API Gateway might connect to Lambda functions or containers running in ECS.

- Each service plays a different role, and together they create flexible and scalable cloud solutions.

