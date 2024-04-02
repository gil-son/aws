RDS
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/thumbs/2x/aws-rds-logo.png" width="40%">
</div>
<br>
<br>
<p>
Amazon Relational Database Service (RDS) is a scalable, managed database service that simplifies the setup, operation, and scalability of relational databases in the cloud. RDS supports several relational database engines, including MySQL, PostgreSQL, Oracle, SQL Server, and MariaDB.
</p>

RDS offers features such as backup and restore, monitoring, scalability, security, and automated patch management. The service is highly available and fault-tolerant, with support for automatic failover and synchronous and asynchronous replication to ensure data integrity.
<details><summary><h3>Features</h3></summary>
<ul>
    <li><b>Scalability:</b> RDS allows you to increase or decrease database capacity quickly and easily without interruption of service.</li>
    <li><b>Availability:</b> RDS is designed to be highly available and fault-tolerant, with support for automatic failover and synchronous and asynchronous replication.</li>
    <li><b>Backup and restore:</b> RDS provides integrated backup and restore capabilities, allowing you to create automatic and on-demand backups and restore databases from those backups.</li>
    <li><b>Monitoring:</b> RDS offers monitoring features to help track database performance and quickly detect problems.</li>
    <li><b>Patch management:</b> RDS provides automated patch management to keep the database up to date and protected against known security vulnerabilities.</li>
    <li><b>Security:</b> RDS offers advanced security features, including data encryption at rest and in transit, role-based access control, and compatibility with Amazon VPC to protect the database in a virtual private network.</li>
</ul> 
</details>
<details><summary><h3>Terms and Concepts</h3></summary>
<ul>
  <li><b>Relational Database:</b> A relational database is a collection of tables that relate to each other through primary and foreign keys.</li>
  <li><b>Database Instance:</b> A database instance is a copy of the database running on a dedicated server in the cloud. You can configure the database instance size and the amount of associated storage.</li>
  <li><b>Snapshot:</b> A snapshot is a copy of the database data at a particular point in time. You can create snapshots manually or schedule them to be created automatically.</li>
  <li><b>Multi-AZ:</b> The Multi-AZ option creates a synchronous replica of the database in a secondary availability zone, increasing the availability and durability of the database.</li>
  <li><b>Read Replica:</b> A read replica is a copy of the database that can be used for data reading, increasing query scalability and performance.</li>
  <li><b>Endpoint:</b> An endpoint is an entry point for accessing an RDS database. Endpoints are used to connect to RDS database instances.</li>
  <li><b>System Parameters:</b> System parameters control the behavior of RDS database instances. They can be modified to adjust the performance and configuration of the database.</li>
  <li><b>Disaster Recovery Options:</b> RDS offers several disaster recovery options, including automatic backups, manual snapshots, and multi-AZ replication.</li>
  <li><b>Aurora:</b> Amazon Aurora is a MySQL and PostgreSQL-compatible relational database service that offers superior scalability, durability, and performance compared to other RDS databases.</li>
</ul>
</details>

<details><summary><h3>Best Practices</h3></summary>
<ul>
  <li>Correctly define primary keys for tables to ensure scalability and query performance</li>
  <li>Use adequate capacity provisioning to avoid increased costs and decreased query performance</li>
  <li>Use Amazon RDS encryption options to protect confidential data in transit and at rest</li>
  <li>Regularly back up database data and regularly test disaster recovery</li>
  <li>Use Amazon RDS security groups to control database access</li>
  <li>Monitor Amazon RDS performance and usage with Amazon CloudWatch and set alerts for anomalies or security issues</li>
  <li>Use multiple availability zones to increase database availability and durability</li>
  <li>Use Amazon RDS Performance Insights to get a detailed view of database performance and identify bottlenecks</li>
</ul> 

These best practices will help ensure that your Amazon RDS database is optimized for scalability, availability, and security, ensuring that your applications can run effectively and efficiently.
</details>

<details><summary> <h3>Advantage over using RDS versus deploying DB on EC2</h3></summary>
<ul>
  <li> RDS is a managed service:
    <ul>
      <li>Automated provisioning, OS patching</li>
      <li>Continous backups and restore to specific timestamp (Point in Time to Restore)!</li>
      <li>Monitoring dashboards</li>
      <li>Read replicas for improved read performance</li>
      <li>Maintenance windows for upgrades</li>
      <li>Scaling capability (vertical and horizontal)</li>
      <li>Storage backed by EBS</li>
    </ul>
  </li>
  <li>BUT you can't SSH into your instances</li>
</ul>

#### RDS Solution Architecture 

<div align="center">
  <img src="https://thumbs2.imgbox.com/ac/c1/huoLe6f2_t.png">
</div>


</details>


