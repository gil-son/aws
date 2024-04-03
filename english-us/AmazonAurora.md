Aurora

<div align="center">
  <img src="https://bluesentry.cloud/wp-content/uploads/2021/02/amazon_aurora.png" width="40%">
</div>
<br>
<br>
<p>
Amazon Aurora is a MySQL and PostgreSQL-compatible relational database service provided by AWS. It offers superior scalability, durability, and performance compared to other RDS databases.
</p>

Aurora's architecture is designed to provide high performance and availability for database workloads. It uses a distributed, fault-tolerant storage system replicated across multiple Availability Zones (AZs) for increased reliability.
<details><summary><h3>Features</h3></summary>
<ul>
    <li><b>Scalability:</b> Aurora provides seamless and automatic scaling to handle growing workloads without downtime.</li>
    <li><b>High Availability:</b> Aurora is built for high availability with automated failover and continuous backups to ensure data durability.</li>
    <li><b>Performance:</b> Aurora offers high performance with a purpose-built storage system and distributed architecture optimized for database workloads.</li>
    <li><b>Compatibility:</b> Aurora is compatible with MySQL and PostgreSQL, allowing easy migration of existing applications and tools.</li>
    <li><b>Backups and Restore:</b> Aurora offers continuous backups and point-in-time recovery, allowing you to restore your database to any second within your retention period.</li>
    <li><b>Security:</b> Aurora provides advanced security features including encryption at rest and in transit, IAM database authentication, and VPC support.</li>
    <li><b>Comparation:</b> Aurora is "AWS optimized" and claims 5x performance improvement over MySQL on RDS, over 3x the performance of Postgres on RDS</li>
    <li><b>Cost:</b> Not in the free tier</li>
</ul> 
</details>
<details><summary><h3>Terms and Concepts</h3></summary>
<ul>
  <li><b>Cluster:</b> An Aurora cluster consists of a primary instance and up to 15 read replicas. The primary instance handles write operations while read replicas can be used for read scaling and failover.</li>
  <li><b>Instance:</b> An Aurora instance is a single endpoint in an Aurora cluster. It can be a primary instance or a read replica.</li>
  <li><b>Storage:</b> Aurora uses a distributed storage system that automatically scales up to 128 terabytes per database instance. It provides consistent, high performance and durability.</li>
  <li><b>Endpoint:</b> An endpoint is a network address that clients use to connect to an Aurora database instance.</li>
  <li><b>Automatic Failover:</b> Aurora automatically detects and replaces a primary instance in case of failure, minimizing downtime.</li>
  <li><b>Performance Insights:</b> Aurora Performance Insights helps you monitor database performance and analyze performance issues in real-time.</li>
</ul>
</details>
<details><summary><h3>Best Practices</h3></summary>
<ul>
  <li>Design tables and indexes to leverage Aurora's distributed architecture for optimal performance.</li>
  <li>Regularly monitor database performance using Aurora Performance Insights and set up alerts for performance anomalies.</li>
  <li>Use IAM database authentication to securely manage database access and eliminate the need for database passwords.</li>
  <li>Enable encryption at rest and in transit to protect sensitive data stored in Aurora databases.</li>
  <li>Regularly test backups and point-in-time restores to ensure data recoverability in case of failure.</li>
  <li>Implement multi-AZ deployments to increase availability and fault tolerance.</li>
  <li>Scale read operations using Aurora read replicas to offload read traffic from the primary instance.</li>
</ul> 
These best practices will help optimize the performance, availability, and security of your Aurora database, ensuring reliable operation for your applications.
</details>

<details><summary> <h3>Advantage over using Aurora versus deploying DB on EC2</h3></summary>
<ul>
  <li> Aurora is a managed service:
    <ul>
      <li>Automated provisioning, OS patching</li>
      <li>Continuous backups and point-in-time recovery</li>
      <li>Monitoring dashboards and Performance Insights</li>
      <li>Read replicas for improved read performance</li>
      <li>Maintenance windows for upgrades</li>
      <li>Scaling capability (vertical and horizontal)</li>
      <li>Storage with automatic scaling and durability</li>
    </ul>
  </li>
  <li>But you can't SSH into your instances</li>
</ul>

#### Aurora Solution Architecture 

<div align="center">
  <img src="https://thumbs2.imgbox.com/6a/f6/RxlEsCvg_t.png">
</div>

</details>

<details><summary> <h3>Amazon Aurora Serverless</h3></summary>

Amazon Aurora Serverless is a cloud-native, on-demand configuration of Amazon Aurora that automatically adjusts database capacity to match application needs. It offers seamless scalability and cost efficiency by automatically scaling up or down based on actual usage. With Aurora Serverless, users no longer need to manage database instances, making it ideal for applications with unpredictable or variable workloads.

<ul>
    <li>Automated database instation and auto-scaling on actual usage</li>
    <li>PostgreSQL and MySQL are both supported as Aurora Serveless DB</li>
    <li>No capacity plannig needed</li>
    <li>Least management overhead</li>
    <li>Pay per second, can be more cost-effective</li>
</ul>

#### User cases

Aurora Serverless is good for infrequent, interminttent or unpredictable workloads.

Well, from the client perspective, it's super easy. It connects to a proxy fleet that is managed by Aurora. And Aurora, behind the scenes, is going to instantiate database instances when it needs to scale up or down. And these Aurora databases are going to be sharing the same storage volume no matter what. So from an exam perspective, if you see Aurora with no management overhead and so on, think of Aurora Serverless.

<div align="center" width="40%">
  <img src="https://thumbs2.imgbox.com/cd/63/C1daqgj1_t.png">
</div>

</details>


</details>
