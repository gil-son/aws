
<details><summary><h4>What is a server composed of?</h4></summary>
<br>

##### A server is composed by:

- Compute: CPU 
- Memory: RAM 
- Storage: Data
- Database: Store data in a structured way
- Network: Routers, switch, DNS server
  - Network: cables, routers and servers connected with each other
  - Router: a networking device that forwards data packets between computer networks. They know where to send your packets on the internet!
  - Switch: takes a packet and send it to the correct server / client on your network

 <div alignr="center">
<img src="https://thumbs2.imgbox.com/c6/e8/H9K98LHQ_t.png" />
 </div>


##### Not a long time ago, that was the way to build an infrastructure (traditional IT approach):
<div alignr="center">
<img src="https://thumbs2.imgbox.com/4b/02/AKnOfE3s_t.png" />
</div>

##### Problems with traditional IT approach

- Pay for the rent for the data center
- Pay for powe supply, cooling, maintenance
- Adding and replacing hardware takes time
- Scaling is limited
- Hire 24/7 team to monitor the infrastructure
- How to deal with disasters? (easthquake, power shutdown, fire...)

Can all this be externalized? Look at the next topic to learn about it.

</details>


<details><summary><h4>Cloud Computing</h4></summary>
<br>

In our previous discussion, we delved into the resource-intensive nature of building and maintaining physical servers, which often translates to substantial costs and space requirements. Fortunately, exists a more efficient solution for organizing server resources. Cloud computing platforms not only provide enhanced security but also offer a more cost-effective alternative to traditional physical servers and resources.

<div alignr="center" width="50%">
  <img src="https://thumbs2.imgbox.com/0d/20/ts9DxwE4_t.png" />
</div>

A Cloud Computing platform encompasses a comprehensive array of resources, offering not only the capabilities of a traditional server but also an extensive range of additional services. This dynamic environment serves as a hub for various technologies. For example:

- **Host Your Server:**
  - Amazon EC2 (Elastic Compute Cloud): Provides resizable compute capacity in the cloud.
  - Amazon ECS (Elastic Container Service): Highly scalable container orchestration service.

- **Host Your Database:**
  - Amazon RDS (Relational Database Service): Managed relational databases in the cloud.
  - Amazon DynamoDB: A fully managed NoSQL database service.

- **Create Your Networking Infrastructure:**
  - Software Defined Networking (SDN): Modern networking approach that virtualizes and abstracts network infrastructure.
  - Amazon VPC (Virtual Private Cloud): Allows you to provision a logically isolated section of the AWS Cloud.
  - Subnets: Segments of a network, often created within a VPC, to organize and secure resources.

These examples merely scratch the surface of the diverse functionalities available within a cloud computing platform. Whether you need to deploy servers, manage databases, or design intricate networking structures, the cloud provides a versatile and scalable ecosystem for all your technological needs.

Cloud computing brings forth numerous benefits! Keep reading to learn about it!

</details>


<details><summary><h4> Five essential characteristics</h4></summary>
<br>

This cloud model is composed of five essential characteristics:

- <b>On-demand self-service:</b> Users can provision computing resources, such as server instances or storage, as needed without requiring human intervention from the service provider.

- <b>Broad network access:</b> Cloud services are accessible over the network through standard mechanisms, promoting widespread availability. Users can access the services from a variety of devices, such as laptops, smartphones, and tablets.

- <b>Resource pooling:</b> The provider's computing resources are pooled to serve multiple customers, with different physical and virtual resources dynamically assigned and reassigned according to demand. This enables efficient resource utilization and scalability.

- <b>Rapid elasticity:</b> Computing resources can be quickly scaled up or down to accommodate changing workloads. This ensures that the cloud environment is flexible and responsive to varying demands, providing agility for businesses and users.

- <b>Measured service:</b> Cloud systems automatically control and optimize resource usage by leveraging a metering capability at some level of abstraction appropriate to the type of service (e.g., storage, processing, bandwidth, and active user accounts). Resource usage can be monitored, controlled, and reported, providing transparency and allowing users to pay only for the resources they consume.
</details>


<details><summary><h4>Three fundamental drivers of cost with AWS</h4></summary>
<br>

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. These characteristics vary somewhat, depending on the AWS product and pricing model you choose.
</details>



<details><summary><h4>Types of Cloud Computing</h4></summary>
<br>
  
##### Infrastrucure as a Service (IaaS)
  
- Provide building blocks for cloud IT
- Provides networking, computers, data storage space
- Highest level of flexibility
- Easy parallel with traditional on-premises IT
- Example
   <table cellspacing="0" cellpadding="0">
     <tr>
      <td> - Amazon EC2</td>
      <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></td>
     </tr>  
    </table>

##### Plataform as a Service (PaaS)
  
- Removes the need for your organization to manage the underlying infraestructure
- Focus on the deployment and management of you applications
- Example
  <table cellspacing="0" cellpadding="0">
    <tr>
      <td>- Elastic Beanstalk</td>
      <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /></td>
    </tr>
  </table>
  
   
   
##### Software as a Service (SaaS)  
- Completed product that us run and managed by the service provider
- Example   
  <table cellspacing="0" cellpadding="0">
    <tr>
      <td>- Many AWS Services (ex: Rekognition for Machine Learning) </td>
      <td><img width="15%" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQWPOov6TZhY9Lso6rbo4_iFQ7OfEgWgy_Fk_INpumtuiPGjltSfJPYyzlbaIbmAtcbSOQ&usqp=CAU" /></td>
    </tr> 
  </table>

<hr/>
<div alignr="center">
<img src="https://thumbs2.imgbox.com/f0/5b/sI1W8WD7_t.png" />
</div>

</details>

<details><summary><h4>Pricing of the Cloud - Quick Overview</h4></summary>
<br>

AWS has 3 princing fundamentals, following the pay-as-you-go pricing model:

- Compute:
  - Pay for compute time   
    <table>
        <tr>
          <td rowspan="4"><img width="30%" src="https://thumbs2.imgbox.com/65/c8/IMPrp1MZ_t.png" /></td>
        </tr>
        <tr>
        <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /> </td>
        </tr>
        <tr>
        <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /> </td>
        </tr>
        <tr>
        <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /> </td>
        </tr>
    </table>
    
- Storage:
  - Pay for data stored in the Cloud 
      <table>
        <tr>
          <td rowspan="4"><img width="30%" src="https://thumbs2.imgbox.com/57/8c/zH60PUMU_t.png" /></td>
        </tr>
        <tr>
        <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/c0828e0381730befd1f7a025057c74fb-43acc0496e64afba82dbc9ab774dc622.svg" /> </td>
        </tr>
        <tr>
        <td><img width="8%" src="https://seeklogo.com/images/A/amazon-elastic-file-system-logo-E7053CDC9F-seeklogo.com.png" /> </td>
        </tr>
        <tr>
        <td><img width="8%" src="https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/aws-storage/choose-the-right-storage-service/images/75c6bec122ddc0a1a76b0bf99a89cae0_2-c-235-e-2-f-2448-40-c-3-8-c-7-b-e-9753-d-6-b-0-df-5.png" /> </td>
        </tr>
    </table>
    
- Data transfer OUT of the Cloud:
  - Data transfer IN is free
   
    <table>
        <tr>
          <td><img width="25%" src="https://hotmart.s3.amazonaws.com/product_pictures/2b279618-20d6-4514-b9e4-d5feb84bc025/aws.png" /></td>
        </tr>
    </table>

- Solves the expensive issue of traditional IT


</details>


<details><summary><h4>Shared Responsability Model</h4></summary>
<br>

- Customer has responsibility for the security <b>IN</b> the Cloud

- AWS has responsibility for the security <b>OF</b> the Cloud

<div alignr="center">
<img src="https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg" />
</div>


<a href="https://aws.amazon.com/compliance/shared-responsibility-model" >More</a>
</details>


<details><summary><h4>Acceptable Use Policy</h4></summary>
<br>

AWS has policies about the use of platform!

You may not use, or facilitate or allow others to use, the Services or the AWS Site:

- for any illegal or fraudulent activity;
- to violate the rights of others;
- to threaten, incite, promote, or actively encourage violence, terrorism, or other serious harm;
- for any content or activity that promotes child sexual exploitation or abuse;
- to violate the security, integrity, or availability of any user, network, computer or communications system, software application, or network or computing device;
- to distribute, publish, send, or facilitate the sending of unsolicited mass email or other messages, promotions, advertising, or solicitations (or “spam”).



<a href="https://aws.amazon.com/aup/" >More</a>



</details>



<details><summary><h4>How to choose an AWS Region?</h4></summary>
<br>

- Compliance:
  - <b>with data governance and legal requirements:</b> data never leaves a region without your explicit permission 
- Proximity: 
  - <b>to customers:</b> reduce latency
- Available services: 
  - <b>within a Region:</b> new services and new features aren't available in every Region
- Princing: 
  - <b>Princing:</b> princing varies region to region and is transparent in the service princing page

 <div alignr="center">
<img src="https://www.awsgeek.com/AWS-Regions/AWS-Regions.jpg" />
 </div>

</details>

<details><summary><h4>AWS Availability Zones</h4></summary>
<br>

- Each region has many availability zones (usually 3, min is 3, max is 6). Example:
  - ap-southeast-2a 
  - ap-southeast-2b
  - ap-southeast-2c
- Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity
- They're separete from each other, so that, they're isolated from disasters
- They're connected with high bandwidth, ultra-low latency networking

 <div alignr="center">
  <img src="https://thumbs2.imgbox.com/d8/f4/VNzQ8gbj_t.png" />
 </div>

</details>

<details><summary><h4>How can users access AWS?</h4></summary>
<br>
<ul>
  <li>To access AWS, you have three options: 
      <ul>
        <li>AWS Mangement Console (protected by password + MFA)</li>
        <li>AWS Command Line Interface (CLI): protected by access keys:
          <ul>
           <li>A tool that enables you tu interact with AWS services using commands in your command-line shell:
            <div alignr="center">
              <img src="https://i.ytimg.com/vi/FwbavIglhis/maxresdefault.jpg" />
            </div>
            (This is just an illustration. You must not share yourself informations to connect in AWS!)
          </li>
          <li>You can use different types of operating systems to connect to AWS
          <div alignr="center">
            <img src="https://www.thelambdablog.com/img/a-concise-guide-to-setting-up-the-aws-command-line-libraries-on-your-local-development-environment-850x446.png" />
           </div>
          </li>
        </ul>
      </li>
      <li>AWS Software Developer Kit (SDK) - for code: protected by access keys:
          <ul>
            <li>AWS Software Development Kit (AWS SDK)</li>
            <li>Language-specific APIs (set of libraries)</li>
            <li>Enables you to access and manage AWS services programmatically</li>
            <li>Embedded within your application</li>
            <li>Supports
                <ul>
                  <li>SDKs (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)</li>
                  <li>Mobile SDKs (Android, iOS, ...)</li>
                  <li>IoT Device SDKs (Embedded, C, Arduino, ...)</li>
                </ul>
            </li>
          </ul>
      </li> 
    </ul>
  </li>  
  <li>Access Key are generated through the AWS Console</li>
  <li>Users manage their own access keys</li>
  <li>Access Keys are secret, just like a password. Don't share them</li>
  <li>Access Key Id ~= username</li>
  <li>Secret Access Key ~= password</li>
</ul> 
</details>
