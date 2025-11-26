# DATABASES
We did many labs under this topic. Here is a lab I found interesting

## FIRST LAB :Build Your DB Server and Interact With Your DB Using an App
Launch an Amazon RDS DB instance with high availability.

Configure the DB instance to permit connections from your web server.

Open a web application and interact with your database.

# TASK 1
create a security group to allow your web server to access your RDS DB instance. The security group will be used when you launch the database instance

# TASK 2
create a DB subnet group that is used to tell RDS which subnets can be used for the database. Each DB subnet group requires subnets in at least two Availability Zones

# TASK 3
configure and launch a Multi-AZ Amazon RDS for MySQL database instance.

# TASK 4
open a web application running on my web server and configure it to use the database

# What I Learned

During this lab, I gained hands-on experience working with Amazon RDS and connecting it to a web application. I learned how to launch an Amazon RDS database that is configured for high availability, which means the database stays reliable even if something goes wrong behind the scenes. AWS automatically handles backups and failover, so the database continues running without major disruption.

I also opened a web application and connected it to the database so it could read information from the RDS instance and write new data back into it. Seeing the database and the application communicate in real time helped me understand how cloud based applications store, update, and retrieve information behind the scenes.

# Overall

This lab gave me a clear understanding of how to create a database in AWS and link it to a functional website. It showed me how the pieces fit together and how modern applications use databases to power features like user data, product listings, or any stored information an app depends on



