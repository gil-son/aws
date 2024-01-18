EC2
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/aws-ec2-logo-svg-vector.svg" width="25%">
</div>

Amazon EC2 (Elastic Compute Cloud) is a cloud computing service that provides scalable computing capacity on Amazon's cloud. It allows you to easily set up and run virtual servers in Amazon's cloud, called EC2 Instances. With Amazon EC2, you can scale your computing capacity vertically or horizontally according to your application needs, paying only for the resources you use.

EC2 = Elastic Compute Cloud = Infrastructure as a Service

It mainly consists in the capability of:

<ul>
    <li>Renting virtual machines (EC2).</li>
    <li>Storing data on virtual drivers (EBS).</li>
    <li>Distribuiting load across machines (ELB).</li>
    <li>Scaling the services using an auto-scaling group (ASG).</li>
</ul> 


<details><summary> <h3>Features</h3></summary>
<hr/>
<ul>
    <li><b>Elasticity:</b> EC2 allows you to scale your computing capacity vertically or horizontally according to your application needs.</li>
    <li><b>Flexibility:</b> EC2 offers a wide selection of instance types, operating systems, databases, and other software options for you to choose from.</li>
    <li><b>Integration with other AWS services:</b> EC2 can be easily integrated with other AWS services, such as Amazon S3, Elastic Load Balancing, Amazon RDS, and others.</li>
    <li><b>Security:</b> EC2 offers advanced security features, such as instance isolation, data encryption, user authentication, and much more.</li>
    <li><b>Management:</b> EC2 allows you to easily manage your instances, with features such as Amazon EC2 Auto Scaling and Amazon EC2 Systems Manager.</li>
</ul> 
<hr/>
</details>
<details><summary> <h3>Components and Configuration</h3></summary>
 <hr/>
 <p>EC2 Instances has so much components and resources:</p>
   <details><summary> <h3>Operating System</h3></summary>
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
    </ul>
  </details>
    
  <details><summary> <h3>Security group (Firewall rules)</h3></summary>
    <ul>
        <li>Security Group are the fundamental of network security in AWS</li>
        <li>They control how traffic is allowed into or out EC2 Instance:
        <div align="center"> 
        <img src="https://thumbs2.imgbox.com/71/d4/653laO96_t.png" />  
        </div>
        </li>
        <li>Security groups contain <b>allow rules</b></li>
        <li>Security groups rules can reference by IP or by security group</li>
        <li>Security groups are acting as a "firewall" on EC2 Instances</li>
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
              So we have our EC2 Instance and it has one security group allow attached to it
              that has inboud rules and outbound rules. So our computer is going to be authorized on say port 22.
              So the traffic can go through from our computer to the EC2 Instance, but someone else's computer, that's
              not using my IP address beacause they don't live where I live (They don't have the same IP), then if they're to                   access our EC2 Instance they will not get through it, because the firewall is going to block it and it will be a                  time out. Then for the outbound rules by default, our EC2 Instance for any security group is going to be by default               allowing any traffic out of it. So our EC2 Instance, id tries to access a website and initiate a connection it is                 going to be allowed by the security group:
            <img src="https://thumbs2.imgbox.com/8b/ab/I2BjxQMv_t.png" /> 
              <br/>
              (So this is the basics of how the firewall works) 
               <hr/>
               About other securty groups. So we have an EC2 Instance, and it has a security group, what I call group number one, and the inbound rules is basically saying, I'm authorizing security group number one inbound and security group number two. So, why would we even do this? 
               Well, if we launch another EC2 Instance and it has security group two attached to it, well, by using security group (instinct) rule we bassically allow our EC2 Instance to go connect straight through on the port we decided onto our first EC2 Instance.
              Similarly, if we have another EC2 Instance with a security group one attached, while we've also authorized this one to communicate straight back to our instances. And so regardless of the IP of our EC2 Instances because they have the right security group
              attached to them they're able to communicate straight through to other instances. And that's awesome because it doesn't make you think about IPs all the time. As well as if you have another EC2 Instance maybe with security group number three attached to it, well,
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
        <li>Does live "outside" the EC2 - if traffic is blocked the EC2 Instance won't see it</li>
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
<li>
    <b>Convention:</b> AWS has the following naming convention:  <em>m</em><b>5</b>.2xlarge
    <ul>
      <li><em>m</em>: instance class</li>
      <li><b>5</b>: generation (AWS improves them over time)</li>
      <li>2xlarge: size within the instance class</li>
    </ul>
</ul>

</details>

  <details><summary> <h3>Instance Types</h3></summary>

  EC2 offers a wide selection of instance types, each with different CPU, memory, storage, and networking capabilities.
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
          </div>
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

  </details>
  
  <details><summary> <h3>AMI images</h3></summary>

  <p>AMI images:</b> Amazon Machine Images (AMI) are pre-configured images that you can use to launch EC2 Instances. They contain the operating system, necessary software, and application settings.</p>
    <ul>
        <li> AMI are a customization of an EC2 Instance
             <ul>
              <li>You add your own software, configuration, operation system, monitoring...</li>
              <li>
                Faster boot / configuration time because all your software is pre-packaged
              </li>
          </ul>
        </li>
        <li>
          AMI are built for a <b>specific region</b> (and can be copied across regions)
        </li>
        <li>
           You can launch EC2 Instances from:
            <ul>
            <li>A Public AMI: AWS provided</li>
            <li>You own AMI: you make and maintain them yourself</li>
            <li>An AWS Marketplace AMI: an AMI someone else made (and potentially sells)</li>
          </ul>
        </li>
        <li>
           AMI Process (from an EC2 Instance):
            <ul>
            <li>Start an EC2 Instance and customize ir</li>
            <li>Stop the instance (for data integrity)</li>
            <li>Build an AMI - this will also create EBS snapshots</li>
            <li>Launch a instances from others AMIs
              <hr/>
              So exist a EC2 Instance in us-east-1a and the same instance as us-east-b
              <div align="center"> 
                <img src="https://thumbs2.imgbox.com/9d/35/d3mKBbbJ_t.png">  
              </div>
              <hr/>
              the proccess consist to launch the instance in us-east-1a, but are necessary customize, then create an AMI from it
              <div align="center"> 
                <img src="https://thumbs2.imgbox.com/ff/d8/5SdUhHBy_t.png">  
              </div>
              <hr/>
              this will be you custom AMI. And then in us-east-1b you will be able to launch from that AMI. It is a copy of your EC2 Instance
              <div align="center"> 
                <img src="https://thumbs2.imgbox.com/22/28/0HABL0sI_t.png">  
              </div>
            </li>  
          </ul>
        </li>
    </ul>
  
  </details>
  
  <details><summary> <h3>EC2 Image Builder</h3></summary>
    
  <p>EC2 Image Builder</p>
    <ul>
      <li>Used to automate the creation of Virtual Machines or container images</li>
      <li>Automate the creation, maintain, validate and test EC2 AMIs, and more</li>
      <li>Can be run on a schedule (weekly, whenever packages are updated, etc...)</li>
      <li>Free service (only pay for the underlying resources)</li>
      <li>Example:
        <hr/>
          So we have the EC2 Image Builder service and we're going to set it up. And it is automatically when it's going to run
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/c0/49/IuhxLYM2_t.png">  
            </div>
        <hr/>
          it is going to create an EC2 Instance called Builder EC2 Instance.
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/aa/f3/bgy59Cv0_t.png">  
            </div>
        <hr/>
          And that EC2 Instance is going to build components and customize the software. For example, install Java, update the CLI, update the software system,
          maybe install firewalls, whatever you define to happen on that EC2 Instance, maybe install your application.
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/b8/1c/DEjZt2tk_t.png">  
            </div>
        <hr/>
          An then once this is done, then an AMI is going to be created out of that EC2 Instance, but all of this is obviously automated.
         Then the AMI is created, but we want to validate it. 
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/de/f3/NtWjFoR1_t.png">  
            </div>
        <hr/>
          So EC2 Image Builder will automatically create a test EC2 Instance from that AMI and going to run a bunch of tests that you are defining in advance.
          And if you don't wanna run any tests, you can just skip that test. But the test can be asking, is the AMI working? Is it secure? Is my application running correctly?
          All these kind of things. 
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/68/15/BOE3J1if_t.png">  
            </div>
        <hr/>
          And then one the AMI is tested, then the AMI is going to be distributed, so while EC2 Image Builder is a regional service, it is possible for you to take that AMI and
          distribute it to multiple regions, therefore, allowing your application and workflow to be truly global. Next, EC2 Image Builder can be run on a schedule. So you can define a weekly schedule,
          or you can say you can run whenever packages are updated, or you can run it manually, etc. And it is a free service. So you're only going to pay for the underlying resources. What's means? That              means that if you create an EC2 Instance during this process, an EC2 Image Builder will create these EC2 Instances, then you're going to pay for these EC2 Instances. And when the AMI
          is created and distribuited youre going to pay for these storage of that AMI wherever it has been created, and wherever it has been distribuited.
            <div align="center">  
              <img src="https://thumbs2.imgbox.com/b9/ae/h2K8lKjU_t.png">  
            </div>
      </li>
    </ul>
  </li>
 
</details>

<details><summary> <h3>EBS - Instance Store</h3></summary>
  <ul>
    <li>EBS volumes are network drives with good but "limited" performance</li>
    <li>If you need a high-performance hardware disk, use EC2 Instance Store</li>
    <li>Better I/O performance</li>
    <li>EC2 Instance Store lose their storage if they're stopped (ephemeral)</li>
    <li>Good for buffer / cache / scratch data / temporary content</li>
    <li>Risk of data loss if hardware fails</li>
    <li>Backupds and Replication are your responsability</li>
  </ul>
</details>


<details><summary> <h3>EFS - Elastic File System</h3></summary>
  <ul>
    <li>Managed NFS (network file system) that can ben mounted on 100s of EC2</li>
    <li>EFS works with Linux EC2 instances in multi-AZ</li>
    <li>Highly available, scalabe, expensive, pay per use, no capacity planning</li>
  
   <hr/>
     <p>
       In this diagram exist an EFS File System with a security group, and then we have EC2 instances in various availability zones connected to it.
       So, we have EC2 instances in us-east-1a, EC2 instances in us-east-1b as well as EC2 instances in us-east-1c. And they're all connected to the same EFS system:
     </p>
      <div align="center"> 
            <img src="https://thumbs2.imgbox.com/2e/2f/j6bLDISQ_t.png">  
      </div>
        <hr/>
    <li> EFS Infrequent Access (EFS-IA)
      <ul>
        <li>Storage class that is cost-optimized for files not accessed every day</li>
        <li>Lower cost compared Standard</li>
        <li>EFS Will automatically move your files to EFS-IA based on the last time they were accessed</li>
        <li>Enable EFS-IA with a Lifecycle Policy</li>
        <li>Example: move files that are not accessed for 60 days to EFS-IA</li>
        </ul>
          <div align="center"> 
                <img src="https://thumbs2.imgbox.com/e3/33/VrvdXrru_t.png">  
          </div>
        <hr/>
    </li>
  </ul>
</details>

<details><summary> <h3>EBS vs EFS</h3></summary>
   <p>
     Look a EBS with EC2 instance in one AZ and another one. Then the EBS volume can only be attached to one instance in one specific AZ. And the EBS volumes are bound to specific availability zones.
     But if we wanted to move over the EBS volume from one AZ to another, we could create a snapshot, it would create an EBS snapshot and then restore that snapshot into a new availability zone.
     And effectively we would've moved the EBS volume over. But this is a copy, this is not an in-sync replica. This is a copy, and that would mean that this drive can now be used by another EC2 instance:
   </p>
  <div align="center"> 
      <img src="https://thumbs2.imgbox.com/1c/74/e3OiEdv8_t.png">  
  </div>
  <hr/>
  <p>
    EFS is a network file system. That means that whatever is on EFS drive is shared by everything that is mounted to it. SO, what does that mean? Say we have many instances in Availability Zone one on one
    or many instances as weell on Availability Zone 2. At the same time, all these instances can mount the same EFS drive, using a mount target, and they will all see the same files.
    So, that makes it a shared file system:
  </p>
  <div align="center"> 
      <img src="https://thumbs2.imgbox.com/36/ac/gg8CtxzO_t.png">
  </div>
  <hr/>
</details>

<details><summary> <h3>FSx</h3></summary>
  <ul>
    <li>Launch 3rd party high-performance file systems on AWS</li>
    <li>Fully managed service</li>
    <li>Currently exist 3 types of FSx
        <ul>
          <li>FSx for Windows File Server
            <ul>
              <li>A fully managed, highly, reliable, and scalable Windows native shared file system</li>
              <li>Built on Windows File Server</li>
              <li>Supports SMB protocol & Windows NTFS</li>
              <li>Integrated with Microsoft Active Directory</li>
              <li>Can be accessed from AWS or your on-premise infrastructure</li>
            </ul>
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/ab/7c/USeaqi2h_t.png">
            </div>
            <hr/>
          </li>
          <li>FSx for Lustre
            <ul>
              <li>A fully managed, high-performance, scalable file storage for <b>High Performance Computing (HPC)</b></li>
              <li>The name Lustre is derived from "Linux" and "cluster"</li>
              <li>Machine Learning, Analytics, Video Processing, Financial Modeling...</li>
              <li>Scales up to 100s GB/s, millions of, sub-ms latencies</li>
            </ul>
            <div align="center"> 
                <img src="https://thumbs2.imgbox.com/3f/29/oDflKIeQ_t.png">
            </div>
          </li>
          <li>FSx for NetApp ONTAP
            <ul>
                <li>A fully managed cloud service that provides highly available and scalable shared storage with advanced data management capabilities.</li>
                <li>Based on the NetApp ONTAP storage operating system, offering enterprise-grade features for data management, efficiency, and security.</li>
                <li>Supports NFS (Network File System) and SMB (Server Message Block) protocols, making it suitable for a wide range of applications and workloads.</li>
                <li>Provides advanced data management features such as data deduplication, data compression, and snapshot-based backups, enhancing storage efficiency and data protection.</li>
                <li>Integrates seamlessly with your existing on-premise NetApp environment, enabling hybrid cloud scenarios.</li>
                <li>Allows you to easily migrate and replicate data between on-premise NetApp systems and FSx for NetApp ONTAP in AWS.</li>
            </ul>
            <div align="center"> 
                <img src="https://github.com/gil-son/aws/assets/72712095/073c464d-5857-4e20-96db-d8fd66a26170">
            </div>
        </li>
      </ul>
    </li>
   </ul>
  <hr/>
  
</details>


<details><summary><h3>Scalability & Availability</h3></summary>
   <details><summary><h4>Scalability</h4></summary>
        <ul>
          <li>Scalability means that application / system can handle greater loads by adapting.</li>
          <li>There are two kinds of scalability:
            <ul>
              <li>Vertical Scalability
                <ul>
                  <li>Vertical Scalability means increase the size of the instance</li>
                  <li>Improve any part of the instance</li>
                  <li>Your application runs on a t2.micro, Scaling that application vertically means running it on a t2.large</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/d4/1a/yPfIV4ZR_t.png">
                  </div>
                  <li>Vertical scalability is very common for non distributed systems, such as a database.</li>
                  <li>Theres usually a limit to how much you can vertically scale (hardware limit)</li>
                </ul>
              </li>
              <li>Horizontal Scalability (= elasticity)
                  <ul>
                  <li>Horizontal Scalability means increase the number of the instance / system for your application</li>
                  <li>Horizontal scaling implies distributed systems</li>
                  <li>This is very common for web applications / modern applications</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/1e/13/1NerXmnE_t.png">
                  </div>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
  </details> 
  <details><summary><h4>Availability</h4></summary>
      <ul>
          <li>High Availability usually goes hand in hand with horizontal scaling</li>
          <li>High availability means running your application / system in at least 2 Availability Zones</li>
          <li>The goal of high availability is to survive a data center loss (disaster)</li>
            <div align="center">
                  <img src="https://thumbs2.imgbox.com/78/63/coxLKVbv_t.png">
            </div>
            <div align="center">
                  <img src="https://thumbs2.imgbox.com/c6/b3/Sjg8TioT_t.png">
            </div>
      </ul>
   </details> 
 </details>

<details><summary><h3>Scalability & Availability For EC2</h3></summary>
      <ul>
          <li>Vertical Scaling: Increase instance size (= scale up / down)
            <ul>
              <li>From: t2.nano - 0.5 of RAM, 1 vCPU</li>
              <li>To: u-12tb.metal - 12.3TB of RAM, 448 vCPUs</li>
            </ul>
          </li>       
          <li>Horizontal Scaling: Increase number of instances (= scale out/ in)
            <ul>
              <li>Auto Scaling Group</li>
              <li>Load Balancer</li>
            </ul>
        </li>
        <li>High Availability: Run instances for the same application across multi AZ:
            <ul>
              <li>Auto Scaling Group multi AZ</li>
              <li>Load Balancer multi AZ</li>
            </ul>
        </li>
      </ul>
</details>





  <p><b>Load Balancers:</b> EC2 offers load balancers, which distribute network traffic among multiple EC2 Instances in a region.</p>
  <p><b>Regions:</b> EC2 is available in several regions around the world. Each region is an independent geographic area, with multiple availability zones to increase resilience and availability.</p>
  <p><b>Availability zones:</b> Each EC2 region has multiple availability zones, which are physically separate data centers, but connected by a low-latency, high-bandwidth network.</p>
  <p><b>Elastic IP:</b> An Elastic IP is a static IP address that you can associate with an EC2 Instance. It allows you to keep the same IP address even if the instance is stopped or restarted.</p>
  <hr/>
</details>

<details><summary> <h3>Best Practices</h3></summary>
<hr/>
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
      <hr/>
      <table>
        <tr>
          <th>Purchasing Option</th>
          <th>Description</th>
        </tr>
        <tr>
          <td>On-Demand Instances</td>
          <td>Short workload, predictable pricing, pay by second</td>
        </tr>
        <tr>
          <td>Reserved Instances (1 & 3 years)</td>
          <td>
            - Reserved Instances: Long workloads with a fixed term commitment<br>
            - Convertible Reserved Instances: Long workloads with flexible instances
          </td>
        </tr>
        <tr>
          <td>Savings Plans (1 & 3 years)</td>
          <td>Commitment to an amount of usage, suitable for long workloads</td>
        </tr>
        <tr>
          <td>Spot Instances</td>
          <td>Short workloads, cost-effective but less reliable</td>
        </tr>
        <tr>
          <td>Dedicated Hosts</td>
          <td>Book an entire physical server, control instance placement</td>
        </tr>
        <tr>
          <td>Dedicated Instances</td>
          <td>No other customers will share your hardware</td>
        </tr>
        <tr>
          <td>Capacity Reservations</td>
          <td>Reserve capacity in a specific AZ for any duration</td>
        </tr>
    </table>
  </li>
  <li>Configure security groups to restrict access to the instance</li>
  <li>Use SSH keys to authenticate access to the instance</li>
  <li>Implement regular backups of the instance to protect critical data</li>
  <li>Monitor the usage of the instance and set alerts for anomalies or performance issues</li>
  <li>Use Elastic Load Balancing to distribute workload across multiple instances and improve availability</li>
  <li>Use Auto Scaling to increase or decrease instance capacity based on workload demand, allowing the infrastructure to adjust automatically to user demand</li>
  <li>Configure security options such as CloudTrail and CloudWatch to monitor and audit access to the instance and protect against security threats</li>
</ul>
<hr/>
</details>

<details><summary> <h3>Responsibility Model for EC2</h3></summary>
<hr/>
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
          <li>Software and utilities installed on the EC2 Instance</li>
          <li>IAM Roles assigned to EC2 & IAM user access management</li>
          <li>Data security on your instance</li>
      </ul>
    </td>
  </tr>
</table>
<hr/>
</details>

<details><summary> <h3>Responsibility Model for EC2 Storage</h3></summary>
<hr/>
<table>
  <tr>
    <th>AWS</th>
    <th>USER</th>
  </tr>
  <tr>
    <td>
        <ul>
          <li>Infrastructure</li>
          <li>Replication for data for EBS volumes & EFS drives</li>
          <li>Replacing faulty hardware</li>
          <li>Ensuring their employees cannot access your data</li>
        </ul>
    </td>
    <td>
       <ul>
          <li>Setting up backup / snapshot procedures</li>
          <li>Setting up data encryption</li>
          <li>Responsibility of any data on the drives</li>
          <li>Understanding the risk of using EC2 Instance Store</li>
      </ul>
    </td>
  </tr>
</table>
<hr/>
</details>
