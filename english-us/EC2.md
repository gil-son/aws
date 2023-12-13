EC2
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/aws-ec2-logo-svg-vector.svg" width="25%">
</div>

Amazon EC2 (Elastic Compute Cloud) is a cloud computing service that provides scalable computing capacity on Amazon's cloud. It allows you to easily set up and run virtual servers in Amazon's cloud, called EC2 instances. With Amazon EC2, you can scale your computing capacity vertically or horizontally according to your application needs, paying only for the resources you use.

EC2 = Elastic Compute Cloud = Infrastructure as a Service

It mainly consists in the capability of:

<ul>
    <li>Renting virtual machines (EC2).</li>
    <li>Storing data on virtual drivers (EBS).</li>
    <li>Distribuiting load across machines (ELB).</li>
    <li>Scaling the services using an auto-scaling group (ASG).</li>
</ul> 


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
<li><b>Sizing and Configurations options:</b> EC2 instances are configurable virtual servers that you can launch on Amazon's cloud:
    <ul>
    <li><b>Operating System (OS):</b> Linux, Windows or Mac OS</li>
    <li>How much compute power & cores (CPU).</li>
    <li>How much random-access memory (RAM).</li>
    <li>How much storage space:
        <ul>
          <li>Network-attached (EBS & EFS)</li>
          <li>hardware (EC2 Instance Store)</li>
        </ul>
    <li><b>Network card:</b> speed of the card, Public IP address</li>
    <li><b>Security group (Firewall rules):</b>
      <ul>
        <li>Security Group are the fundamental of network security in AWS</li>
        <li>They control how traffic is allowed into or out EC2 Instance:
        <div align="center"> 
        <img src="https://thumbs2.imgbox.com/71/d4/653laO96_t.png" />  
        </div>
        </li>
        <li>Security groups contain <b>allow rules</b></li>
        <li>Security groups rules can reference by IP or by security group</li>
        <li>Security groups are acting as a "firewall" on EC2 instances</li>
        <li>They regulate:  
          <ul>
            <li>Access to Ports</li>
            <li>Authorised IP ranges - IPv4 and IPv6</li>
            <li>Controll of inbound network (from other to the instance)</li>
            <li>Controll of outbound network (from other to the instance)</li>
            <div align="center"> 
            <img src="https://thumbs2.imgbox.com/9f/5d/nGp5IhhT_t.png" />  
              <hr/>
              Source represents an IP address range and 0.0.0.0/0 means everything
              (That is an illustration. Then don't share your particular informations)
              <hr/>
              So we have our EC2 instance and it has one security group allow attached to it
              that has inboud rules and outbound rules. So our computer is going to be authorized on say port 22.
              So the traffic can go through from our computer to the EC2 instance, but someone else's computer, that's
              not using my IP address beacause they don't live where I live (They don't have the same IP), then if they're to                   access our EC2 instance they will not get through it, because the firewall is going to block it and it will be a                  time out. Then for the outbound rules by default, our EC2 instance for any security group is going to be by default               allowing any traffic out of it. So our EC2 instance, id tries to access a website and initiate a connection it is                 going to be allowed by the security group:
            <img src="https://thumbs2.imgbox.com/8b/ab/I2BjxQMv_t.png" /> 
              <br/>
              (So this is the basics of how the firewall works) 
               <hr/>
               About other securty groups. So we have an EC2 instance, and it has a security group, what I call group number one, and the inbound rules is basically saying, I'm authorizing security group number one inbound and security group number two. So, why would we even do this? 
               Well, if we launch another EC2 instance and it has security group two attached to it, well, by using security group (instinct) rule we bassically allow our EC2 instance to go connect straight through on the port we decided onto our first EC2 instance.
              Similarly, if we have another EC2 instance with a security group one attached, while we've also authorized this one to communicate straight back to our instances. And so regardless of the IP of our EC2 instances because they have the right security group
              attached to them they're able to communicate straight through to other instances. And that's awesome because it doesn't make you think about IPs all the time. As well as if you have another EC2 instance maybe with security group number three attached to it, well,
              because it group number three, was't authorized in the inbound rules of security group number one, then it's being denied and things don't work. So that's a bit of an advanced feature. Whereas it's can be usefull with load balancers:
              <br/>
              <img src="https://thumbs2.imgbox.com/26/2c/GV6J2skK_t.png" />  
            </div> 
              The notation "203.0.113.0/24" in CIDR represents a range of IP addresses from 203.0.113.0 to 203.0.113.255. The "/24" indicates that the first 24 bits are the network portion, and the remaining 8 bits are available for host addresses.
              So, when you specify "203.0.113.0/24" as the source in your security group rule, it covers all IP addresses from 203.0.113.0 to 203.0.113.255, inclusive. Therefore, both 203.0.113.001 and 203.0.113.002 are part of this range.
              <br/>
                <ul>
                  To clarify:
                  <li>203.0.113.0 is the network address.</li>
                  <li>203.0.113.255 is the broadcast address.</li>
                  <li>The range of usable IP addresses is from 203.0.113.1 to 203.0.113.254.</li>
                  <li>IP addresses outside of this range, such as 203.0.114.0 aren't acceptable.</li>
                </ul>
          </ul>
        </li>
        <li>Locked down to a region / VPC combination</li>
        <li>Does live "outside" the EC2 - if traffic is blocked the EC2 instance won't see it</li>
        <li>It's good to maintain one separete security group for SSH access</li>
        <li>If your application is not accessible (time out), then it's a security group issue</li>
        <li>If your application gives a "connection refused" error, then it's an application error or it's not launched</li>
        <li>All inbound traffic is blocked by default</li>
        <li>All outbound traffic is authorised by default</li>
        <li> Classic Ports to know
          <ul>
            <li>22 = SSH (Secure Shell) - log into a Linux instance.</li>
            <li>21 = FTP (File Transfer Protocol) - upload files into a file share.</li>
            <li>22 = SFTP (Secure File Transfer Protocol) - upload files using SSH.</li>
            <li>80 = HTTP (Hypertext Transfer Protocol) - access unsecured websites.</li>
            <li>443 = HTTPS (Hypertext transfer protocol secure) - access secured websites </li>
            <li>3389 = RDP (Remote Desktop Protocol) - log into Windows instance</li>
          </ul>
        </li>
      </ul> 
    </li>  
    <li><b>Bootsrap script (configure at first launch):</b>EC2 User Data.</li>
  </ul> 
</li>
<li><b>AMI images:</b> Amazon Machine Images (AMI) are pre-configured images that you can use to launch EC2 instances. They contain the operating system, necessary software, and application settings.</li>
<li>
<b>Convention:</b> AWS has the following naming convention:  <em>m</em><b>5</b>.2xlarge
  <ul>
    <li><em>m</em>: instance class</li>
    <li><b>5</b>: generation (AWS improves them over time)</li>
    <li>2xlarge: size within the instance class</li>
  </ul>
</li>
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
<a href="https://aws.amazon.com/ec2/instance-types/"/> More information</a>
</ul>
</li>
<li><b>Regions:</b> EC2 is available in several regions around the world. Each region is an independent geographic area, with multiple availability zones to increase resilience and availability.</li>
<li><b>Availability zones:</b> Each EC2 region has multiple availability zones, which are physically separate data centers, but connected by a low-latency, high-bandwidth network.</li>
<li><b>Elastic IP:</b> An Elastic IP is a static IP address that you can associate with an EC2 instance. It allows you to keep the same IP address even if the instance is stopped or restarted.</li>
<li><b>Load Balancers:</b> EC2 offers load balancers, which distribute network traffic among multiple EC2 instances in a region.</li>
</ul>
</details>
<details><summary> <h3>Best Practices</h3></summary>
<ul>
  <li><b>Purchasing Option:</b> Choose the appropriate instance type based on the computing resource needs and expected workload:
    <ul>
      <li>On-Demand Instances - short workload, predictable princing, pay by second</li>
      <li>Reserved (1 & 3 years)
        <ul>
          <li>Reserved Instances - long workloads</li>
          <li>Convertible Reserved Instances - long workloads with flexible instances</li>
        </ul>
      </li>
      <li>Savings Plans (1 & 3 years) - commitment to an amount of usage, long workload</li>
      <li>Spot Instances - short workloads, cheap, can lose instances (less reliable)</li>
      <li>Dedicated Hosts - book an entire physical server, control instance placement</li>
      <li>Dedicated Instances - no other customers will share you hardware</li>
      <li>Capacity Reservations - reserve capacity in a specific AZ for any duration</li>
    </ul>
  </li>
  <li>Configure security groups to restrict access to the instance</li>
  <li>Use SSH keys to authenticate access to the instance</li>
  <li>Implement regular backups of the instance to protect critical data</li>
  <li>Monitor the usage of the instance and set alerts for anomalies or performance issues</li>
  <li>Use Elastic Load Balancing to distribute workload across multiple instances and improve availability</li>
  <li>Use Auto Scaling to increase or decrease instance capacity based on workload demand, allowing the infrastructure to adjust automatically to user demand</li>
  <li>Configure security options such as CloudTrail and CloudWatch to monitor and audit access to the instance and protect against security threats</li>
</ul>
</details>

<details><summary> <h3>Responsibility Model for EC2</h3></summary>

<table>
  <tr>
    <th>AWS</th>
    <th>USER</th>
  </tr>
  <tr>
    <td>
        <ul>
          <li>Infrastructure (global network security)</li>
          <li>Isolation on physical host</li>
          <li>Replacing faulty hardware</li>
          <li>Compliance validation</li>
        </ul>
    </td>
    <td>
       <ul>
          <li>Security Groups rule</li>
          <li>Operating-system patches and updates</li>
          <li>Software and utilities installed on the EC2 instance</li>
          <li>IAM Roles assigned to EC2 & IAM user access management</li>
          <li>Data security on your instance</li>
      </ul>
    </td>
  </tr>
</table>

</details>
