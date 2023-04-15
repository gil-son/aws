DynamoDB

<div align="center">
  <img src="https://www.datarain.com.br/wp-content/uploads/2020/08/DybamoDB-logo.png" width="35%">
</div>
Amazon DynamoDB is a fully managed and scalable NoSQL database that provides high-performance and low-latency storage and data retrieval. DynamoDB is designed to be a highly available and fault-tolerant database solution capable of handling large volumes of data and read/write traffic.

<details><summary><h3>Features</h3></summary>
<ul>
    <li><b>Scalability:</b> DynamoDB can automatically and quickly scale horizontally without service interruption to support large volumes of data and traffic.</li>
    <li><b>Performance:</b> DynamoDB offers very high data read and write performance, with millisecond latencies.</li>
    <li><b>Availability:</b> DynamoDB is designed to be highly available, with synchronous and asynchronous data replication to ensure fault tolerance.</li>
    <li><b>Access management:</b> DynamoDB offers granular access control features, allowing you to define table and table item access permissions based on IAM roles, access policies, and access keys.</li>
    <li><b>Backup and restoration:</b> DynamoDB offers built-in backup and restoration features, allowing you to create automatic and on-demand backups of tables and restore tables from those backups.</li>
</ul> 
</details>
<details><summary><h3>Terms and Concepts</h3></summary>
<ul>
<li><b>Tables:</b> DynamoDB is a NoSQL database, and all information is stored in tables. Each table contains multiple rows (items), and each row can have a variable number of columns (attributes).</li>
<li><b>Partitions:</b> DynamoDB is designed to be highly scalable, and data is distributed into partitions to ensure high availability and performance. Each partition is a set of items that share the same partition key.</li>
<li><b>Primary Key:</b> Each item in a DynamoDB table must have a unique primary key that identifies the item. There are two types of primary key in DynamoDB: partition key and partition key and sort key.</li>
<li><b>Sort Key:</b> The sort key is an additional attribute that can be used to sort items within a partition.</li>
<li><b>Indexes:</b> DynamoDB supports two types of indexes: key indexes and global indexes. Key indexes are created based on one or more attributes of the table, while global indexes allow queries on any attribute of the table.</li>
<li><b>Consistency:</b> DynamoDB supports two consistency options for reads: strong consistency and eventual consistency.</li>
<li><b>Capacity:</b> DynamoDB is horizontally scalable and allows you to adjust read/write capacity to meet your application's performance needs. Read/write capacity is measured in read/write units, and you can provision the amount of units needed to meet your application's traffic requirements.</li>
<li><b>Streams:</b> DynamoDB Streams is a feature that allows you to capture changes to DynamoDB tables in real-time and process them using AWS services such as AWS Lambda.</li>
<li><b>Querying and Filtering:</b> DynamoDB allows you to use query and filtering expressions on a table.</li>
<li><b>Transactions:</b> DynamoDB supports atomic transactions that allow you to group multiple operations into a single transaction.</li>
</ul>
</details>

<details><summary> <h3>Best Practices</h3></summary>
<ul>
  <li>Correctly define primary keys for tables to ensure scalability and query performance</li>
  <li>Use appropriate capacity provisioning to avoid increased costs and decreased query performance</li>
  <li>Use DynamoDB encryption options to protect sensitive data</li>
  <li>Use transactions to maintain data consistency in complex operations involving multiple tables or items</li>
  <li>Configure appropriate access control policies to limit access to tables</li>
  <li>Use Amazon CloudWatch to monitor DynamoDB performance and usage, and set alerts for anomalies or security issues</li>
</ul>
</details>
