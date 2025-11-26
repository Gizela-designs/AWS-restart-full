# Database Basics

- A database is essentially a highly organized digital system for storing and managing information. You can think of it as a very advanced filing cabinet where data is arranged so it can be easily found, updated, and protected.

- There are two major categories of databases. Relational databases, often called SQL databases, store data in a structured and predictable layout that resembles multiple linked Excel spreadsheets. Each table contains rows and columns, and everything follows strict rules, which is ideal for situations where accuracy and relationships matter, such as banking systems, inventory records, or student information systems. Non relational databases, also called NoSQL databases, handle information in a more flexible way. Instead of tables, they may use documents, key value pairs, or graphs. These databases are perfect for use cases like social media profiles or e commerce catalogs where each item might look different and doesn’t follow a rigid format.

- A few fundamental database concepts help everything stay organized. A schema defines the layout and rules for your data, similar to a blueprint. The primary key is a unique identifier for every record, such as a student number or a product ID. An index works like the index at the back of a book, helping the database quickly locate specific information without searching through everything.
 
## Amazon Aurora, the high performance relational database

Aurora is Amazon’s enhanced version of popular databases like MySQL and PostgreSQL. It is built specifically for the cloud and offers significant improvements in speed, reliability, and automation. Aurora is known for being several times faster than standard MySQL and for its ability to automatically back up your data, repair itself when something breaks, and expand its storage as your application grows. Aurora Serverless is a version designed for unpredictable workloads. It automatically turns itself on and off and adjusts its size based on demand, so you only pay when your application is actively using it. This makes it ideal for student projects, new startups, or applications that experience big swings in traffic.
 
## Amazon DynamoDB, the fully managed NoSQL powerhouse

- DynamoDB is Amazon’s highly scalable NoSQL database designed for applications that need extremely fast performance even at massive scale. It can handle millions of requests every second and still respond almost instantly. Since AWS manages all the underlying servers, you never need to worry about hardware, patching, or maintenance. DynamoDB automatically scales to match your traffic, which makes it ideal for gaming applications, mobile apps, and large ecommerce systems.

- Data in DynamoDB is stored in tables, which contain items, and each item is made up of attributes. Everything inside is located using a primary key. DynamoDB also offers two capacity modes. On Demand allows you to pay only for each read or write, making it excellent for unpredictable workloads or new applications. Provisioned capacity allows you to specify how much traffic you expect, which can reduce costs when your workload is steady and predictable.
 
## Choosing the right database

The best database depends on the type of data and the needs of your application. If your information naturally fits into tables and needs strong consistency or relationships, a relational database such as Aurora is usually the right match. If your application expects rapid growth, unpredictable traffic, or needs extreme scalability with flexible data structures, DynamoDB is often the better option. For applications that require complex queries or the ability to join information from multiple tables, Aurora will usually provide better functionality. If your goal is to achieve fast lookups for simple data such as product IDs or session information, DynamoDB excels in that area. Workloads that shift between quiet and busy periods can benefit from Aurora Serverless or DynamoDB On Demand, since both adapt to changing demand automatically.

## Getting data in and out of your database

- Relational databases like Aurora use SQL commands. To retrieve information, you use the SELECT command and can narrow your results using conditions such as WHERE country equals USA. SQL also allows you to join multiple tables so that related information can be shown together. Adding new data is done with the INSERT command, which places a new row into your table.

- DynamoDB handles data differently. Retrieving information usually involves making a Query or GetItem request that searches by key or by a particular attribute. This method is extremely fast, though it is not designed for complex relationships. Adding information is done with PutItem for single records or BatchWriteItem when you want to insert many items at once. Using the batch method is more efficient and reduces the number of individual requests your application needs to make. 
 
 
 
 
 