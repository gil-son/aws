EC2
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/aws-ec2-logo-svg-vector.svg" width="25%">
</div>

Amazon EC2 (Elastic Compute Cloud) is a cloud computing service that provides scalable computing capacity on Amazon's cloud. It allows you to easily set up and run virtual servers in Amazon's cloud, called EC2 instances. With Amazon EC2, you can scale your computing capacity vertically or horizontally according to your application needs, paying only for the resources you use.
<details><summary> <h3>Features</h3></summary>
<ul>
    <li><b>Elasticity:</b> EC2 allows you to scale your computing capacity vertically or horizontally according to your application needs.</li>
    <li><b>Flexibility:</b> EC2 offers a wide selection of instance types, operating systems, databases, and other software options for you to choose from.</li>
    <li><b>Integration with other AWS services:</b> EC2 can be easily integrated with other AWS services, such as Amazon S3, Elastic Load Balancing, Amazon RDS, and others.</li>
    <li><b>Security:</b> EC2 offers advanced security features, such as instance isolation, data encryption, user authentication, and much more.</li>
    <li><b>Management:</b> EC2 allows you to easily manage your instances, with features such as Amazon EC2 Auto Scaling and Amazon EC2 Systems Manager.</li>
</ul> 
</details>
<details><summary> <h3>Terms and Concepts</h3></summary>
<ul>
<li><b>Instances:</b> EC2 instances are configurable virtual servers that you can launch on Amazon's cloud.</li>
<li><b>AMI images:</b> Amazon Machine Images (AMI) are pre-configured images that you can use to launch EC2 instances. They contain the operating system, necessary software, and application settings.</li>

<li>
<b>Instance Types:</b> EC2 offers a wide selection of instance types, each with different CPU, memory, storage, and networking capabilities.
<div align="center"> 
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20220322144908/typesofec2instances768x384.png" width="70%">  
</div>
<ul>
<li><b>General Purpose:</b>
  <ul>
    <li>Balances compute, memory, and networking resources.</li> 
    <li>Recommended for application servers, gaming, backend, small databases.</li>
  </ul>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/ac/37/XseN96S8_t.png">  
</div>  
 </li>
<li><b>Compute Optimized:</b>  
  <ul>
    <li>Ideal for workloads that require high-performance processors.</li> 
    <li>Can be used for the same use cases as general purpose but when higher performance is desired.</li>
    <li>Also ideal for batch processing.</li>
<div align="center"> 
<img src="https://news.mit.edu/sites/default/files/styles/news_article__image_gallery/public/images/202001/MIT-Evaluating-Performance_0.jpg?itok=qVXPQAya" width="50%">  
  </ul>
 </li>
</li>
<li><b>Memory Optimized:</b> 
    <ul>
    <li>Designed for high performance in processing large amounts of in-memory data.</li> 
    <li>For example, high-performance databases, real-time data processing.</li>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/85/bb/AEbPZHGd_t.png">  
</div>      
  </ul>
</li>
<li><b>Accelerated Computing:</b> 
  <ul>
    <li>Uses hardware acceleration or coprocessors to perform certain functions more efficiently than in software running directly on the CPU.</li> 
    <li>Commonly used for floating-point calculations, graphics processing, and data pattern matching.</li>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/33/18/Sg9mLdO3_t.png">  
</div>
  </ul>
</li>
<li><b>Storage Optimized:</b> 
  <ul>
    <li>Ideal for workloads that require high read and write access to large volumes of data.</li> 
    <li>Commonly used in distributed file systems, data warehouses, online transaction processing systems.</li>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/76/f9/NAK8q2sT_t.png">  
</div>
  </ul>
</li>  
</ul>
</li>
<li><b>Regions:</b> EC2 is available in several regions around the world. Each region is an independent geographic area, with multiple availability zones to increase resilience and availability.</li>
<li><b>Availability zones:</b> Each EC2 region has multiple availability zones, which are physically separate data centers, but connected by a low-latency, high-bandwidth network.</li>
<li><b>Elastic IP:</b> An Elastic IP is a static IP address that you can associate with an EC2 instance. It allows you to keep the same IP address even if the instance is stopped or restarted.</li>
<li><b>Load Balancers:</b> EC2 offers load balancers, which distribute network traffic among multiple EC2 instances in a region.</li>
</ul>
</details>
<details><summary> <h3>Best Practices</h3></summary>

Some best practices for using EC2 include:
<ul>
  <li>Configuring appropriate access control policies to limit access to stored objects</li>
  <li>Using S3 encryption options to protect sensitive data</li>
  <li>Setting up lifecycle policies for old and unused objects to reduce costs</li>
  <li>Using versioning and access control options to track and manage changes to stored objects</li>
  <li>Monitoring S3 usage and setting alerts for anomalies or security issues</li>
</ul>
</details>
